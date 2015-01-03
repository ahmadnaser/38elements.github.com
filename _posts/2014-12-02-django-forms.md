---
layout: posts
title: DjangoのFormメモ 
---
* 入力コントロールのidは[auto_id](https://docs.djangoproject.com/en/1.7/ref/forms/api/#django.forms.Form.auto_id)

* エラーメッセージを追加するには[add_error](https://docs.djangoproject.com/en/1.7/ref/forms/api/#django.forms.Form.add_error)を利用する。

* カスタムバリデーションは[clean](https://docs.djangoproject.com/en/1.7/ref/forms/api/#django.forms.Form.clean)に書く

* バリデーションは[is_valid](https://docs.djangoproject.com/en/1.7/ref/forms/api/#django.forms.Form.is_valid)で行う

* デフォルトのエラーメッセージは[error_messages](https://docs.djangoproject.com/en/1.7/ref/forms/fields/#django.forms.Field.error_messages)に定義する

* フィールドに指定する変数一覧 [*](https://docs.djangoproject.com/en/1.7/ref/forms/fields/#core-field-arguments)

* テンプレートでform.foo.valueで値を表示することができる

* formとmodelを関連付ける [*](https://docs.djangoproject.com/en/dev/topics/forms/modelforms/)

* コントロールの属性の指定方法 [*](https://docs.djangoproject.com/en/1.7/ref/forms/widgets/#django.forms.Widget.attrs)

* wigetの一覧 [*](https://docs.djangoproject.com/en/1.7/ref/forms/widgets/)

* wigetの属性を変更する   
form.fields["foo"].widget.attrs["bar"] = "qwert" 

* ModelFormではBooleanFieldはrequired=Falseになっている

* ModelFormでrequired=Falseにする方法    
{% highlight python %}
class Foo(ModelForm):
    def __init__(self, *args, **kwd):
        super(Foo, self).__init__(*args, **kwd)
        self.fields["bar"].required = False
{% endhighlight %}