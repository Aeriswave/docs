# Как начать работать c {{ iam-short-name }}

Сервис {{ iam-short-name }} позволяет вам управлять доступом к ресурсам.

Эта инструкция для [владельцев](../resource-manager/concepts/resources-hierarchy.md#owner) и [администраторов](concepts/access-control/roles.md#admin) облака. Вы научитесь:

* [добавлять пользователей в свое облако](#add-user);
* [назначать пользователям роли](#assign-role);
* [отнимать назначенные роли](#revoke-roles).

## Перед началом

1. Если вы еще не зарегистрированы в Яндекс.Облаке, перейдите в [консоль управления](https://console.cloud.yandex.ru).
1. [На странице биллинга](https://console.cloud.yandex.ru/billing) убедитесь, что у вас подключен [платежный аккаунт](../billing/concepts/billing-account.md) и он находится в статусе `ACTIVE` или `TRIAL_ACTIVE`. Если платежного аккаунта нет, [создайте его](../billing/quickstart/index.md#create_billing_account).
1. Если вам некого добавить в облако, вы можете [создать новый аккаунт](https://passport.yandex.ru/registration) на Яндексе и предоставить доступ в облако для этого аккаунта.

## Добавьте нового пользователя в облако {#add-user}

Чтобы предоставить пользователю доступ к ресурсам, добавьте его в свое облако:

1. {% include [grant-role-console-first-steps](../_includes/iam/grant-role-console-first-steps.md) %}
1. На странице **Пользователи и роли** в правом верхнем углу нажмите **Добавить пользователя**.
1. Введите электронную почту пользователя в Яндексе.
1. Нажмите кнопку **Добавить**.

{% include [roles-cloud-member](../_includes/roles-cloud-member.md) %}

## Назначьте пользователю роли {#assign-role}

Чтобы указать, какие операции можно выполнять пользователю, назначьте ему соответствующие роли. Например, разрешите ему управлять ресурсами в одном из каталогов:

1. {% include [configure-roles-console](../_includes/iam/configure-roles-console.md) %}
1. В блоке **Роли на облако <имя облака>** нажмите ![image](../_assets/plus-sign.svg).
1. Выберите роль `{{ roles-viewer }}`. Эта роль позволит пользователю просматривать ресурсы в вашем облаке.
1. Выберите каталог в блоке **Роли в каталогах** и нажмите ![image](../_assets/plus-sign.svg).
1. Выберите роль `{{ roles-editor }}`. Эта роль позволит пользователю создавать ресурсы в этом каталоге и управлять ими.

## Отнимите назначенные роли {#revoke-roles}

Если назначенные роли больше не нужны, отнимите их:

1. Снова откройте окно настройки ролей:
    1. Откройте страницу [Управление доступом]({{ link-console-access-management }}).
    1. {% include [configure-roles-console](../_includes/iam/configure-roles-console.md) %}
1. Нажмите на крестик возле каждой роли, которую хотите отнять.
1. Нажмите **Закрыть**.

    Если у пользователя не осталось ролей в вашем облаке, он исчезнет из списка.

{% note tip %}

Если вы хотите отнять все роли сразу, [удалите пользователя](operations/users/delete.md) из вашего облака.

{% endnote %}

## Что дальше

* [Пошаговые инструкции](operations/index.md) помогут вам решить конкретные задачи, возникающие при использовании {{ iam-name }}.
* Прочитайте, [как устроено управление доступом в Яндекс.Облаке](concepts/access-control/index.md).
* Узнайте о [способах аутентификации в API](api-ref/authentication.md).
* Посмотрите [ответы на часто задаваемые вопросы](qa/index.md).