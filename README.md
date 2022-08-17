# kubetest2

Запуск:
    go run .\cmd\apiserver\

Тесты:
    go test -v -race -timeout 30s ./...

## Аутентификация

Как таковых, пользователей в кубернетес нет. Но для аутентификации можно использовать
__SSL сертификаты__. В dn которых указывается имя пользователя. В этом случае доступ осуществляется по сертификату.

Подробности создание сертификата пользователя описаны тут: [www.kryukov.biz](https://www.kryukov.biz/2019/10/kubernetes-dostup-po-sertifikatu-polzovatelya/)

Другой вариант доступа, использовать __ServiceAccount__. В этом случае доступ будет осуществляться по токену.

## Роли

Для описания прав доступа можно использовать механизм RBAC.

__Role, ClusterRole__ и __RoleBinding, ClusterRoleBinding__
