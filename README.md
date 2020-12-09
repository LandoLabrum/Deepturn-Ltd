Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@LandoLabrum 
LandoLabrum
/
Deepturn-Ltd
1
00
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Deepturn-Ltd/read.me
@LandoLabrum
LandoLabrum Create read.me
Latest commit 7abb884 14 seconds ago
 History
 1 contributor
22 lines (15 sloc)  555 Bytes

{% extends "forms/field.html.twig" %}

{% block input %}
    <div class="form-textarea-wrapper {{ field.size }}">
        <textarea
            {# required attribute structures #}
            name="{{ (scope ~ field.name)|fieldName }}"
            {# input attribute structures #}
            {% block input_attributes %}
                {% if field.classes is defined %}class="materialize-textarea {{ field.classes }}" {% else %}class="materialize-textarea {{ field.classes|default('input') }}" {% endif %}
                {% if field.id is defined %}id="{{ field.id|e }}" {% endif %}
                {% if field.style is defined %}style="{{ field.style|e }}" {% endif %}
                {% if field.disabled or isDisabledToggleable %}disabled="disabled"{% endif %}
                {% if field.placeholder %}placeholder="{{ field.placeholder|t }}"{% endif %}
                {% if field.autofocus in ['on', 'true', 1] %}autofocus="autofocus"{% endif %}
                {% if field.novalidate in ['on', 'true', 1] %}novalidate="novalidate"{% endif %}
                {% if field.readonly in ['on', 'true', 1] %}readonly="readonly"{% endif %}
                {% if field.autocomplete in ['on', 'off'] %}autocomplete="{{ field.autocomplete }}"{% endif %}
                {% if field.validate.required in ['on', 'true', 1] %}required="required"{% endif %}
                {% if field.validate.pattern %}pattern="{{ field.validate.pattern }}"{% endif %}
                {% if field.validate.message %}title="{% if grav.twig.twig.filters['tu'] is defined %}{{ field.validate.message|tu|e }}{% else %}{{ field.validate.message|t|e }}{% endif %}"{% endif %}
                {% if field.rows is defined %}rows="{{ field.rows }}"{% endif %}
                {% if field.cols is defined %}cols="{{ field.cols }}"{% endif %}
            {% endblock %}
            >{{ value|trim|e('html') }}</textarea>
    </div>
{% endblock %}

# DeepTurn Ltd - Social Automation

The following is a basic analysis over the functionality and schema of the Social Automation product.

## Onboarding

Onboarding is essential and not only provides the User with State-o-the-art insights, but also provides crucial data to improve the overall efficiency of the program as a whole.
Onboarding must be thoroughly completed and must include the following, but is not limited to:
* Login Credentials
* Competative Set
* Ally Set
* Demographic
* Goal
* White List
* Black List

## Process
The over-all schema of the software runs off of a TFX pipeline. a TFX pipeline is a sequence of components that implement an ML pipeline which is specifically designed for scalable, high-performance machine learning tasks.

Stage  | Description
------------- | -------------
Research  | Multiple iterations, with parameters set from the Onboarding Process, ingest and validate large quantities of data including hundreds if not thousands of data-points / post.
Agent Account  | Agent Accounts, combine the power of the ( Research Stage ), as well as the onboarding parameters, to indirectly build an audience of the most-engaged users to 
put them through the ranks.
Collaboration  | After the Users have been incubated and qualified for the clients end-goal, Collaboration with the Agent Account and the Client Account begins. 


* To insure a steady growth, the longer the alogrithm runs on a client, the faster the account will grow. *

## Usage
The Software is always adapting & growing so the algorithms change depending on Instagrams Algorithms, 3rd party Applications and Software may be used to aid the growth of an account. DeepTurn Ltd Provides no warranty, no protection in preparation or during the use of the Service. 


## License
[MIT]()
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
