# 教示点を修正する  
ワークの把持位置を変える、など一度実施した教示を修正する必要は、たびたび発生します。このような場合は登録済マスターがあれば再登録することなく、ロボットの再教示のみ行うことができます。

1. VT動作文脈まで実行  
ステップ動作などで、撮影から解析、VT動作(相対ジョブ)の文脈まで進めます。

{% ifenv env="Motoman" %}
~~~
*CAPTURE
MOVJ VJ=20.00 //撮影位置
TIMER T=0.500
CALL JOB:ROVI_CAPTURE
GETS LI000 $RV
JUMP *CAPTURE IF LI000<>0
*SOLVE
CALL JOB:ROVI_SOLVE (90) //解析結果をP090へ
GETS LI000 $RV
JUMP *SOLVE IF LI000<>0
*VTMOV
MFRAME UF#(1) P090 BF //P090をUF1に設定
CALL JOB:<相対ジョブ>
~~~
{% endifenv %}

2. 教示(VT動作)  
教示モードに切り替えて、VTで設定されたユーザ座標系で教示を行います。

3. 教示(通常動作)  
VTで変換しない動作を教示する場合は、ユーザ座標系を(ユーザ０などに)戻すことを忘れないこと。



