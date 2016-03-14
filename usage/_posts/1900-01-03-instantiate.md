---
title: instantiate
---

Ok, so now that we've got it installed and we have the credentials sorted, let's
instantiate it so we can actually use it!

{% highlight js %}
var dynasty = require('dynasty')(credentials);
{% endhighlight %}

Optionally, provide a `url` as the second argument to connect to a Dynamo
instance that is not on AWS. For example if you are running Dynamo
[locally](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Tools.DynamoDBLocal.html)
you would instantiate it as follows:

{% highlight js %}
var dynasty = require('dynasty')(credentials, 'localhost:8000');
{% endhighlight %}

Note, you still have to provide credentials, even if running locally doesn't
require them because the internal code expects them to be present.

That was easy! But how to query it?
