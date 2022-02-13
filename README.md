# goit-markup-hw-02
hw-02
flex-grow -залитие остатка



background-size: auto | значение | cover | contain
                cover - 
                            Гарантированно сохраняет пропорции изображения.
                            Изображению задаются минимальные размеры, при которых оно зальёт фон всего элемента.
                            Если пропорции изображения и элемента разные, часть изображения, по вертикали или горизонтали, визуально обрезается.
                contain -    Гарантированно сохраняет пропорции изображения, 
                            -Изображению задаются максимально возможнные размеры (не больше оригинала), при которых оно полностью помещается в элемент.
                            -Изображение может не закрыть весь фон элемента по вертикали или горизонтали, если пропорции блока и изображения не совпадают.
                        
background-attachment: scroll| fixed | inherit
                scroll - фон прокручиватеся вместе с содержимым. Это значение по умолчанию.
                fixed - фон не прокручивается, зафиксирован на месте.


background - Составное свойство для одновременного задания значений всех    
             рассмотренных свойств. 
             [background: background-color background-image background-repeat background-position background-attachment]

КОРРЕКЦИЯ ИЗОбРАЖЕНИЯ В КОНТЕЙНЕРЕ

object-fit: fill | contain | cover | scale-down | none

object-fit -    обрезает, растягивает или масштабирует контентное изображение. Это 
                похоже на background-size, но для контентных изображений.

                fill -      изображение масштабируется без сохранения пропорций, 
                            чтобы полностью заполнить контейнер. Значение по умолчанию.
                contain -   изображение масштабируется с сохранением пропорций, чтобы
                            максимально заполнить контейнер.
                cover -     изображение масштабируется с сохранением пропорций, 
                            чтобы полностью заполнить контейнер.
                scale-down- будет выбрано значение none или contain, чтобы 
                            изображение было наименьшего размера.
                none -      сохраняются исходные размеры изображения, 
                            заданная высота и ширина не имеют эффекта.
object-position
                object-position: position | initial | inherit


ПСЕВДОЭЛЕМЕНТЫ
                ::before - создаёт псевдоэлемент перед всем контентом элемента 
                в начале).
                ::after - создаёт псевдоэлемент после всего контента элемента (в конце)

                - строчные

ПСЕВДОКЛАСС
                :hover - 
                        /* Применить стили к псевдоэлементу .box::before при ховере по элементу .box */
                        .box:hover::before {
                        color: green;
                        }

                        /* Применить стили к псевдоэлементу .box::after при ховере по элементу .box */
                        .box:hover::after {
                        color: tomato;
                        }
ГРАДИЕНТ
                Линейный градиент
                        linear-gradient(<направление>, <цвет-1>, <цвет-2>, <цвет-3>, ...)
                            <направление> - to top, to right, to bottom, to left и их комбинациями. Если направление не указано, используется значение по умолчанию - сверху-вниз (to bottom)


                        Колорстоп (color-stop)

                 repeating-linear-gradient
                        background-image: repeating-linear-gradient(
                        to left,
                        blue,
                        blue 20px,
                        red 20px,
                        red 40px /* Опеределяет размер градиента */
                        );

ТЕНЬ ЭЛЕМЕНТА
                box-shadow: inset <x-offset> <y-offset> <blur> <spread> <color>
                x-offset - горизонтальное смещение. Положительное значение смещает тень вправо от блока, отрицательное – влево. Обязательное значение.
                y-offset -  вертикальное смещение. Положительное значение смещает тень
                вниз, отрицательное - вверх. Обязательное значение.
                blur - радиус размытия. Чем больше значение, тем сильнее размыта тень. Необязательное значение.
                spread - радиус распространения. Положительное значение увеличивает тень, отрицательное - уменьшает. Необязательное значение.
                color - цвет тени. Можно использовать любой формат записи цвета. Необязательное значение.




ФОРМЫ
<form>
  <label>
    Email
    <input type="email" name="email" />
  </label>

  <label>
    Password
    <input type="password" name="password" />
  </label>

  <button type="submit">Submit</button>
</form>

Элемент <form> - это контейнер для группы связанных элементов формы.
            Атрибуты
            name - уникальное на текущей веб-странице имя формы. 

            autocomplete - определяет, может ли браузер автоматически заполнять значения всех элементов формы. Имеет всего два значения off и on. Это

            novalidate - атрибут-флаг, не имеет значения. Говорит браузеру не проверять валидность введённых данных при отправке формы. Если атрибут не указан, выполняется клиентская валидация.

            ОТПРАВКА ФОРМЫ
            
            При клике по <button type="submit"> или при нажатии клавиши Enter в любом поле формы, она «отправляется», что приводит к перезагрузке текущей страницы. Это поведение по умолчанию, которое можно будет изменить при помощи JavaScript.



Элемент <label> -  связывает описание (метку) с интерактивным элементом формы. Текст метки связан с элементом не только визуально, но и логически.
            
             <label>
                Email
                <input type="email" name="email" />
            </label>

            <label for="user_email">Email</label>
            <input type="email" name="email" id="user_email" />

Элемент <input> - Универсальный элемент для создания разнообразных полей ввода. 
            Тип поля определяется атрибутом type, значение которого по умолчанию text - однострочное текстовое поле принимающее любые символы.

            Атрибут autofocus - 
                    Поле ввода которому задан этот атрибут автоматически получит фокус при загрузке страницы и в нём можно сразу набирать текст.
            Атрибут placeholder -   
                    текст подсказкаю Этот атрибут можно использовать в    любом элементе формы, где есть текстовый ввод.
            атрибута type
                    email -
                    password - Атрибуты minLength и maxLength
                     <label>
                         Password
                        <input type="password" name="password" minlength="5" maxlength="12" />
                     </label>
            Радио-кнопки (переключатели)
                        атрибуту type значение radio  
                            Радио-кнопки всегда идут группами, что позволяет пользователю выбрать одно из множества предопределенных значений.

                            Каждой радио-кнопке в группе задаётся одинаковое значение атрибута name, иначе браузер не будет знать, что это группа.
                                <label>
                                    <input type="radio" name="color" value="red" checked />
                                    Red
                                </label>
                            Чтобы сделать группу радиокнопок или чекбоксов обязательной, необходимо задать атрибут REQUIRED каждому элементу группы.

            Чекбоксы (флажки) 
                        Флажки (чекбоксы, checkbox) похожи на переключатели, но позволяют выбирать произвольное количество значений, то есть многие из многих.
            Числа
                        тип поля number 
                                    Для того чтобы разрешить вводить только числа, с
            Ползунки
                        Тип range
                                type="range"
                                name="interest_rate"
                                value="40"
                                min="0"
                                max="100"
                                step="20"
            Дата и время -
            ё               В браузерах есть встроенный календарь, в котором пользователь может выбрать требуемую дату и/или время. Атрибуты min и max позволяют установить минимальные и максимальные даты, при условии использования правильного формата.

                                type=date
                                type=time
                                type=datetime-local

                                min="1920-01-01T00:00"
                                max=

Элемент <textarea> -   
            Создаёт многострочное текстовое поле для ввода большого количества текста.
            rows устанавливает количество строк (высоту)
            cols - колонок (ширину).  (На практике указывается только rows)

            resize  both | horizontal | vertical | none
Элемент <select> -
            Выпадающее меню это альтернатива радио-кнопкам, поскольку по умолчанию позволяет выбрать один из многих вариантов. Элемент <select> это раскрывающееся меню с атрибутом name, которое содержит набор элементов <option> с атрибутом value.

            <option> -  отображается пользователю
            <VALUE> - это то, что будет использовано при отправке формы.
            
            selected -   выбран первый элемент по умолчанию


            Группировка опций
                    <optgroup>   Иногда требуется разбить список на отдельные группы, не связанные между собой. Для этих целей есть тег <optgroup>. Чтобы добавить заголовок группы, используется атрибут label.

                        <optgroup label="Summer">
                            <option value="s6">June</option>
                            <option value="s7">July</option>
                            <option value="s8">August</option>
                        </optgroup>

Элемент <datalist>
                        <label for="fav">Choose your favourite browser</label>
                        <input list="browsers" name="fav" id="fav" />
                        <datalist id="browsers">
                        <option>Edge</option>
                        <option>Firefox</option>
                        <option>Chrome</option>
                        <option>Opera</option>
                        <option>Safari</option>
                        </datalist>


Группировка полей

 <fieldset> - группа

 <legend> -  заголовок группі
                        <fieldset>
                            <legend>Enter your contact details</legend>
                            <label>
                            Name
                            <input type="text" name="username" />
                            </label>
                            <label>
                            Email
                            <input type="email" name="email" />
                            </label>
                        </fieldset>
В большинстве случаев для группировки элементов формы используется <div> с атрибутами доступности role и aria-labelledby
                        <div role="group" aria-labelledby="contact-details-head">
                        <p id="contact-details-head">Enter your contact details</p>
                        Related elements
                        </div>




Валидация

Логический атрибут REQUIRED помечает поле формы как обязательное для заполнения.

Ограничение по длине 
    inlength и 
    maxlength накладывают ограничения на количество вводимых символов, 
                <label>
                    Username
                    <input type="text" name="username" required minlength="3" />
                </label>
                <label>
Ограничение значения
    Атрибуты min и max позволяют проверить вхождение численного значения в указанный промежуток. Могут быть использованы только в полях с типом 
    number, 
    range, 
    date.
                <label>
                    How many pizzas do you want to order?
                    <input type="number" name="amount" required min="1" max="10" />
                </label>


Регулярное выражение
            Атрибут pattern позволяет указать регулярное выражение (шаблон) относительно которого будет проверяться значение поля. Используется для расширения базовой валидации. Например, если требуется чтобы имя пользователя состояло из двух слов или пароль содержал хотя бы один символ в верхнем регистре, один в нижнем регистре и одно число.




Псевдоклассы состояния
            Существует набор псевдоклассов, созданных специально для элементов форм, и не оказывающих никакого эффекта на другие элементы. С помощью них можно оформлять поля формы по состоянию валидности введённых данных или обязательности заполнения.


                :enabled и :disabled
:checked    
            Применяется к радиокнопкам и чекбоксам, и позволяет выбрать только отмеченные поля. Например, пусть при выборе чекбокса текст метки становится синим. Используя селектор + можно выбрать метку когда чекбокс отмечен, но для этого необходимо чтобы тег <label> был в разметке после чекбокса.

:required и :optional


:valid и :invalid
                Позволяют выбрать элементы с валидным или невалидным введённым значением. Проверочные ограничения задаются атрибутами type, minlength, maxlength и pattern.
:placeholder-shown  
                Применяется в зависимости от видимости плейсхолдера - значения атрибута placeholder. Вводите текст в поля формы и цвет рамки поля изменится на синий как только пропадёт плейсхолдер.

Композиция псевдоклассов
                .form-input:not(:placeholder-shown):required:valid {
                /* ... */
                }

:focus-within
                Применяется к элементу когда он сам или элементы внутри него получают фокус. В отличие от :focus, который выбирает сам элемент получивший фокус, :focus-within работает для предков. Это позволяет применить стили на метку, форму или отдельные её части, когда пользователь взаимодействует с полями.



ПОЗИЦИОНИРОВАНИЕ

