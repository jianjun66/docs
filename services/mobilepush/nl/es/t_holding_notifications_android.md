---

copyright:
 years: 2015, 2016

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

# Retención de notificaciones para Android
{: #hold-notifications-android}
Última actualización: 06 de diciembre de 2016
{: .last-updated}

Cuando su aplicación entre en segundo plano, probablemente querrá enviar por push el servicio {{site.data.keyword.mobilepushshort}} para retener notificaciones que se envían a la aplicación. Para retener las notificaciones, llame el método hold() en el método onPause() de la actividad que maneja las {{site.data.keyword.mobilepushshort}}.

```
	@Override
protected void onPause() {
    super.onPause();
    if (push != null) {
        push.hold();
    }
	} 
```
	{: codeblock}
