<template>
    <div v-if="show" class="modal-shadow" @click.self="closeModal">
        <div class="modal">
            <div class="modal-close" @click="closeModal">&#10006;</div>
            <slot name="title">
                <h3 class="modal-title">{{ title }}</h3>
            </slot>
            <slot name="content">
                <div class="modal-content" v-if="title === 'Лицензионное соглашение'">
                    <p>1. Общие положения</p>
                    <p>1.1. Настоящее Лицензионное соглашение (далее — «Соглашение») регулирует использование мобильного приложения «Название Приложения» (далее — «Приложение»), разработанного и распространяемого Компанией «Название Компании» (далее — «Компания»).</p>
                    <p>1.2. Компания является владельцем всех прав на Приложение и его исходный код.</p>
                    <p>2. Права и ограничения</p>
                    <p>2.1. Компания предоставляет пользователю неисключительную лицензию на использование Приложения на условиях, изложенных в настоящем Соглашении.</p>
                    <p>2.2. Пользователь имеет право установить и использовать Приложение на одном мобильном устройстве, при условии соблюдения всех условий настоящего Соглашения.</p>
                    <p>2.3. Пользователь не имеет права:</p>
                    <p>Перепродавать, сдавать в аренду или сублицензировать Приложение;</p>
                    <p>Декомпилировать, дизассемблировать, дешифровать или иным образом пытаться получить исходный код Приложения;</p>
                    <p>Модифицировать, изменять или создавать производные работы на основе Приложения.</p>
                    <p>3. Условия использования</p>
                    <p>3.1. Пользователь обязуется использовать Приложение исключительно в законных целях, не нарушая прав третьих лиц и не причиняя вреда репутации Компании.</p>
                    <p>3.2. Пользователь несет полную ответственность за все действия, совершенные с использованием Приложения, и гарантирует, что такие действия соответствуют всем применимым законам и правилам.</p>
                    <p>4. Интеллектуальная собственность</p>
                    <p>4.1. Все права на Приложение, включая исходный код, дизайн, графику, аудиовизуальные материалы и другие элементы, принадлежат Компании.</p>
                    <p>4.2. Любое несанкционированное копирование, распространение или использование материалов, являющихся частью Приложения, является нарушением прав интеллектуальной собственности Компании.</p>
                    <p>5. Отказ от гарантий</p>
                    <p>5.1. Компания не предоставляет никаких гарантий, явных или подразумеваемых, относительно Приложения, включая, но не ограничиваясь, гарантиями товарной пригодности, пригодности для определенной цели и ненарушения прав интеллектуальной собственности.</p>
                    <p>5.2. Компания не несет ответственности за любые прямые, косвенные, случайные, специальные или штрафные убытки, возникшие в результате использования или невозможности использования Приложения.</p>
                    <p>6. Обновления и поддержка</p>
                    <p>6.1. Компания оставляет за собой право периодически выпускать обновления и исправления для Приложения.</p>
                    <p>6.2. Обновления предоставляются на условиях, изложенных в настоящем Соглашении. Установка обновлений означает принятие пользователем условий настоящего Соглашения на момент обновления.</p>
                    <p>7. Изменения в Соглашении</p>
                    <p>7.1. Компания имеет право вносить изменения и дополнения в настоящее Соглашение в любое время.</p>
                    <p>7.2. Новая версия Соглашения вступает в силу с момента ее публикации на указанной странице. Пользователь обязан самостоятельно следить за изменениями и обязуется принять и выполнять все условия новой версии Соглашения.</p>
                    <p>8. Контакты</p>
                    <p>8.1. Для вопросов, связанных с настоящим Соглашением или использованием Приложения, пользователь может связаться с Компанией по следующим контактам:</p>
                    <p>Электронная почта: email@example.com</p>
                    <p>Телефон: номер телефона</p>
                    <p>9. Заключительные положения</p>
                    <p>9.1. Настоящее Соглашение регулируется и толкуется в соответствии с законодательством страны, в которой зарегистрирована Компания.</p>
                    <p> 9.2. Любые споры и разногласия, возникающие из или в связи с настоящим Соглашением, будут разрешаться путем переговоров между сторонами. В случае невозможности разрешения споров путем переговоров, они подлежат рассмотрению в компетентном суде страны, в которой зарегистрирована Компания.</p>
                    <p>Благодарим вас за использование нашего Приложения и надеемся на ваше понимание и сотрудничество.</p>
                </div>
                <div class="modal-content" v-if="title === 'Политика конфиденциальности'">
                    <p>1. Введение</p>
                    <p>Настоящая Политика конфиденциальности (далее — «Политика») определяет, как [Название Компании] (далее — «Компания») собирает, использует и защищает личную информацию пользователей мобильного приложения [Название Приложения] (далее — «Приложение»).</p>
                    <p>2. Сбор личной информации</p>
                    <p>2.1. Компания собирает следующую личную информацию:</p>
                    <p>Адрес электронной почты</p>
                    <p>2.2. Личная информация собирается только с согласия пользователя, за исключением случаев, когда это необходимо для предоставления услуг или выполнения договорных обязательств.</p>
                    <p>3. Использование личной информации</p>
                    <p>3.1. Компания использует личную информацию для следующих целей:</p>
                    <p>Улучшение качества обслуживания</p>
                    <p>Персонализация контента и предложений</p>
                    <p>Анализ поведения пользователей для улучшения функционала Приложения</p>
                    <p>Отправка уведомлений и обновлений</p>
                    <p>3.2. Компания не продает личную информацию третьим лицам.</p>
                    <p>4. Защита личной информации</p>
                    <p>4.1. Компания принимает все необходимые меры для защиты личной информации от несанкционированного доступа, использования и раскрытия.</p>
                    <p>4.2. Личная информация хранится на защищенных серверах и передается по зашифрованным каналам связи.</p>
                    <p>5. Права пользователей</p>
                    <p>5.1. Пользователи имеют право на доступ к своей личной информации, ее исправление и удаление.</p>
                    <p>5.2. Пользователи могут запросить ограничение или прекращение обработки их личной информации в любое время.</p>
                    <p>6. Изменения в Политике конфиденциальности</p>
                    <p>6.1. Компания оставляет за собой право вносить изменения в настоящую Политику конфиденциальности.</p>
                    <p>6.2. Все изменения будут опубликованы на этой странице, и пользователи могут в любой момент ознакомиться с актуальной версией Политики.</p>
                    <p>7. Контакты</p>
                    <p>7.1. Если у вас возникли вопросы или предложения по поводу настоящей Политики конфиденциальности, вы можете связаться с нами по адресу:</p>
                    <p>Электронная почта: [email@example.com]</p>
                    <p>Телефон: [номер телефона]</p>
                    <p>Мы благодарим вас за использование нашего Приложения и ценим ваше доверие.</p>
                </div>
            </slot>
            <slot name="footer">
                <div class="modal-footer">
                    <button class="modal-footer_button" @click="closeModal">
                        Ок
                    </button>
                </div>
            </slot>
        </div>
    </div>
</template>
 
<script>
    export default {
        name: "ModalWindow",
        data: function () {
            return {
                title: "Заголовок",
                show: false
            }
        },
        methods: {
            closeModal: function () {
                this.show = false

            },
            openModal: function (title) {
                this.show = true;
                this.title = title;
            }
        }
    }
</script>
 
<style scoped>
    .modal-shadow {
        position: fixed;
        top: 0;
        left: 0;
        min-height: 100%;
        width: 100%;
        background: rgba(0, 0, 0, 0.39);
    }
 
    .modal {
        background: #fff;
        border-radius: 8px;
        padding: 15px;
        min-width: 420px;
        max-width: 50%px;
        max-height: 90%;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .modal-close {
        border-radius: 50%;
        color: #fff;
        background: #000000;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        top: 7px;
        right: 7px;
        width: 30px;
        height: 30px;
        cursor: pointer;
    }
 
    .modal-title {
        color: #000000;
    }
 
    .modal-content {
        margin-bottom: 20px;
        overflow: scroll;
        color: rgb(0, 0, 0);
        max-height: 70vh;
    }
 
    .modal-footer {
        &__button {
            background-color: #0971c7;
            color: #fff;
            border: none;
            text-align: center;
            padding: 8px;
            font-size: 17px;
            font-weight: 500;
            border-radius: 8px;
            min-width: 150px;
        }
    }
</style>