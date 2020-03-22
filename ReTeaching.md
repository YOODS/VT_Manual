# 教示点を修正する

## 1.VT動作までステップ実行  
~~~
CALL JOB:ROVI_CAPTURE

CALL JOB:ROVI_SOLVE (90) //解析結果をP090へ

MFRAME UF#(1) P090 BF //P090をUF1に設定

CALL JOB:<相対ジョブ>
~~~
