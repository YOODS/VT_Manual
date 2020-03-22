# ロボットコントローラの設定

{% ifenv env="Fanuc" %}
!INCLUDE "SetupFanuc.md"
{% endifenv %}
{% ifenv env="Motoman" %}
!INCLUDE "SetupMotoman.md"
{% endifenv %}
{% ifenv env="Melfa" %}
!INCLUDE "SetupMelfa.md"
{% endifenv %}
