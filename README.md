# Домашнее задание к занятию 2 «Работа с Playbook»

## Подготовка к выполнению

1. Изучил ClickHouse и Vector, в том числе по видео на Youtube.

2. Создан публичный репозиторий https://github.com/Granit16/ansible-02

3. В нем воссоздан playbook задания.

4. В качестве хостов созданы ВМ на ОС Fedora 37



## Основная часть

1. Подготовил файл **prod.yml**, описал в нем host clickhouse-01 (ВМ)

2. Дописал несколько тасков: `Get vector distrib`, `Install vector packages` и `Config vector`.
    Конфигурация деплоится из шаблона **/templates/vector.yml**.
    Создан `handler: Restart vector service`, который перезапускает vector после изменения конфигурации.

3. При создании тасков были использованы `get_url`, `template`.

4. Таски качают дистрибутив `vector`, устанавливают его и конфигуриурет из шаблона.

5. <details><summary>Результат выполнения команды `ansible-lint site.yml`</summary>
    
    Ошибок нет, имеются несклолько предупреждений

    ![](https://github.com/Granit16/ansible-02/blob/main/screenshots/lint.png)

</details>
