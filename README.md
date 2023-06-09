# GUI-Apps (some examples)
Здесь описаны некоторые из моих проектов, имеющие GUI. В основном представленны те проекты, в которых я являюсь автором и единственным разработчиком.

## Qualia (2019, 2022)
Программа для создания и наблюдения за работой нейронных сетей с линейной регрессией. Я использую эту программу как "песочницу" для изучения математики нейронных сетей и оптимизации C#-кода для высокой производительности.
Функции:
- Динамическое добавление/удаление нейронов, слоёв и сетей.
- Выбор функции активации для каждого нейрона.
- Реализованы три задачи: подсчет количества точек на поле, подсчет крестиков на поле, распознавание рукописных символов MNIST. Другие задачи могут быть легко добавлены.
___

- С#/WPF.
- Pet-проект.

<img width="1280" alt="2022-07-27 (5)" src="https://user-images.githubusercontent.com/53271533/230772367-da8f5f68-14ce-4335-afad-d4a6c26356f7.png">

<img width="1280" alt="2022-07-24 (14)" src="https://user-images.githubusercontent.com/53271533/230772364-e1ab7aa1-cee0-4050-b57e-068316bcf50a.png">

<img width="1280" alt="2022-06-01" src="https://user-images.githubusercontent.com/53271533/230772496-218efb5e-b0ab-40ed-9dcb-4a9744e38efc.png">

Old version video example:
[![Watch the video](https://img.youtube.com/vi/uWcIvifTGrY/maxresdefault.jpg)](https://youtu.be/uWcIvifTGrY)

## MCG - Mobile/Multy-Protocol Call Generator - мультипротокольный генератор трафика (2006-2008, 2013-2015)
Мультипротокольный генератор трафика на основе XML-сценариев. Представляет собой машину выполнения сценариев, описанных в XML-формате. Сценарии представляют собой описание машин состояний различных протоколов. В описание входит посылка протокольных сообщений с различными параметрами, прием сообщений и их обработка в зависимости от значений входящих параметров, контроль таймеров ожидания событий, взаимодействие с терминалом MCGM (GUI-монитор), контроль скорости в любых точках сценариев с выводом на внешний монитор, логирование сообщений об ошибках, логирование изменений состояний, использование программных точек остановки (breakpoint) для программной отладки, запуск других приложений и многие другие функции. Сценарии могут запускать другие сценарии в зависимости от успешности или неуспешности своего выполнения, что позволяет создавать тестовые сценарии какой угодно сложности и отслеживать их выполнение как на консоли, так и на внешнем GUI-мониторе MCGM, который создает отчеты о текущей сессии тестирования. Все это позволяет полностью автоматизировать тестирование кода (ночные билды и тесты, тесты после вноса изменений в систему контроля версий исходного кода).

Изначально проект задумывался как эмулятор радио-подстсемы мобильной сети 2G/3G по протоколу SS7 поверх TCP/IP и UDP, позднее функции были расширены для эмуляции трафика любых протоколов поверх TCP/IP и UDP. Оптимизирован для высокой производительности, имеет отладочный и нагрузочный режим работы. Генератор легко расширяется для тестирования любых протоколов поверх TCP/IP и UDP.

Как приложение генератор представляет собой Windows-консоль. В 2013 году получил элементы графического интерфейса в виде кнопок часто используемых утилит, встроенной информационной системы, а также раскраску сообщений консоли. В 2014 году в него был встроен математический процессор, что позволило оптимизировать сценарии и внести в них такие элементы программирования, как циклы и сценарии-функции. Изначально сценарии поддерживают обьявление и использование переменных и констант. В 2015 году в генератор был встроен HTTP-сервер для получения отчетов и управления генерацией через любой web-браузер.

- С++, MFC, XML, HTTP/CSS/JavaScript.
- Проект был начат в 2006 году, как неофициальный, для помощи разработчикам Intertel. После подтверждения своей эффективности был официально принят в разработку и внедрен в рабочие процессы компании. Использование генератора позволило формализовать стадию тестирования, что в свою очеред позволило оптимизировать процессы разработки и внедрить в компании методологию Scrum, т.к. успешное прохождение всех тестов подтверждало успешное завершение спринтов. Для тестирования новых функций ПО был нанят QA-специалист, который работал с этим генератором. В 2013 году ситуация повторилась для компании Sitronics/NVision. Проект был успешно внедрен в процессы компании. Кроме того, с 2013 года в генератор была добавлена возможность и сценарии для непосредственного тестирования протоколов TCAP, MAP, CAP, ISUP.
- Автор и единственный разработчик.

Общий вид консоли генератора.

![unnamed (3)](https://user-images.githubusercontent.com/53271533/230766912-0a09f27f-e36d-4812-ae61-386ef0cb9931.png)

Встроенный валидатор XML-сценариев показывает ошибки в сценариях. Синтаксические ошибки показываются пользователю вместе с контекстом (частью XML-файла с ошибкой), что позволяет легко находить и исправлять ошибки в сценариях, такие, как незакрытый XML-тег, синтаксические ошибки и т.д.

![unnamed](https://user-images.githubusercontent.com/53271533/230766907-140462b0-5087-468d-8e24-02e7a0b23d05.png)

Встроенные таблицы структуры протокольных сообщений показываются пользователю в виде всплывающих подсказок, что позволяет QA-сотруднику всегда иметь под рукой информацию из официальных рекомендаций IEEE.

![unnamed (1)](https://user-images.githubusercontent.com/53271533/230766908-9425d12f-824a-4c8c-aa3d-e4c7d4757454.png)

Встроенная система расшифровки аббревиатур в виде всплывающих подсказок. Облегчает работу тестера и разработчика, помогая ориентировать в различных аббревиатурах протоколов.

![unnamed (2)](https://user-images.githubusercontent.com/53271533/230766911-917aa922-d960-4237-8d42-c9930974a891.png)

Встроенный конвертер цифровых значений.

![unnamed (4)](https://user-images.githubusercontent.com/53271533/230766913-8942f93f-fc28-402d-97ba-e8f9df832ff8.png)

HTTP-интерфейс для управления и наблюдения за параметрами генератора и трафика.

![unnamed (6)](https://user-images.githubusercontent.com/53271533/230766917-7f6d56bd-e678-4079-a491-5816c57226f9.png)

Примеры HTTP-отчета о работе генератора трафика. Все отчеты формируются в реальном времени.

![unnamed (10)](https://user-images.githubusercontent.com/53271533/230766910-b451bfbb-caa2-4975-87a7-dacedf362fd7.png)

![unnamed (8)](https://user-images.githubusercontent.com/53271533/230766921-c406f8b1-22d1-4bb6-8337-2fe3e426e0e1.png)

![unnamed (9)](https://user-images.githubusercontent.com/53271533/230766922-d114597b-ab64-4865-9937-b61a3d9ce09d.png)

Пример XML-сценария:

    <Scenario Name="CAP_CALL" StateHolder="CAP::GetSession">
      <State Name="Begin">
        <OnState>
          <Do Action="PA::CallBegin" Context="var::GlobalCorrelator" />

          <Do Action="CAP::AssignTraceId" If="var::GlobalCorrelator == -1" />
          <Do Action="CAP::SetTraceId" />

          <Do Action="Var" LocalCorrelator="if (var::GlobalCorrelator == -1, PA::Current, var::GlobalCorrelator)" TraceChange="All" />
          <Do Action="Var" GlobalCorrelator="-1" TraceChange="All" />

          <Do Action="CAP::CreateDialoguePortion" Name="AppContext" AppContext="0.4.0.0.1.0.50.1" />
          <Do Send="CAP::InitialDP_CALL"
                        SK="117"
                        EventType="const::Event_AnalyzedInformation"
                        CallingNumber="PA::CallingNumber"
                        CallingNP="1"
              
                        RedirectOnConnect="1"
                        CalledNumber="PA::CalledNumber"
                        CalledNP="1"
                        CalledINN="0"
                        CalledNAI="4"
              
                        IMSI="PA::IMSI"
                        CallReferenceNumber="PA::CallReferenceNumber"
                        VLRNumber="79168999903abcde"
                        MSCAddress="79168999904abcde"
                        MSCAddressType="0"
                        MSCAddressPlan="0"
                        CellGlobalIdOrServiceAreaId="00 00 00 02 4e c7 00"
                        DialoguePortion="AppContext"
                        AgeOfLocationInformation="0"
                        iPSSPCap="01"
                        TimeAndZone="Now" />
          <Do State="InitialWait" />
        </OnState>
      </State>

      <State Name="InitialWait">
        <OnState>
          <Do Timer="30" />
        </OnState>
        <OnTimer>
          <Do Status="Unsucc" />
          <Do Action="PA::CallEnd" Status="Timeout" />
          <Do Action="End" />
        </OnTimer>
        <Gets>
          <Get Msg="TCAP::ContinueIndication">
          </Get>
          <Get Msg="CAP::RequestReportCALLEvent">
            <Do Action="Var" AnswerMessageType="CAP::MessageTypeFromMonitorMode(CAP::MonitorMode(const::Event_Answer))" />
            <Do Action="Var" DisconnectMessageType="CAP::MessageTypeFromMonitorMode(CAP::MonitorMode(const::Event_Disconnect))" />
          </Get>
          <Get Msg="CAP::ContinueCALL">
            <Do Send="CAP::EventReportCALL" EventType="const::Event_Answer" MessageType="var::AnswerMessageType" />
            <Do Send="TCAP::ContinueRequest" />
            <Do State="Continue" />
          </Get>

          <!-- A new call must be started (new IDP with Destination number, redirecting info, original party number, redirect) -->
          <Get Msg="CAP::ConnectCALL"> 
            <Do Action="Var" GlobalCorrelator="var::LocalCorrelator" />
            <Do Action="Var" HardLimit="PA::HardLimit" TraceChange="All" />
            <Do CallBack="CB_CAP_CALL_REDIRECT" If="PA::NotHardLimit" />
            <Do State="HardLimit" If="var::HardLimit" />
          </Get>

          <!-- A new call must be started as temporary connection to an assistant -->
          <Get Msg="CAP::EstablishTemporaryConnection">
            <Do Action="Var" LocalCorrelator="PA::Current" If="var::LocalCorrelator == -1" />
            <Do Action="Var" GlobalCorrelator="var::LocalCorrelator" />
            <Do Action="Var" HardLimit="PA::HardLimit" TraceChange="All" />
            <Do CallBack="CB_CAP_REQUEST_ASSISTANT" If="PA::NotHardLimit" />
            <Do State="HardLimit" If="var::HardLimit" />
          </Get>

          <Get Msg="TCAP::EndIndication">
          </Get>
          
          <Get Msg="CAP::ApplyChargingCALL">
          </Get>
          
          <Get OnGet="TCAP::PAbortIndication">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" Status="Unsucc" />
            <Do Action="End" />
          </Get>
          
          <Get Msg="CAP::ReleaseCALL" Cause="16">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" />
            <Do Action="End" />
          </Get>

          <Get Msg="CAP::ReleaseCALL" Cause="31">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" />
            <Do Action="End" />
          </Get>

          <Get Msg="CAP::ReleaseCALL">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" Status="Unsucc" />
            <Do Action="End" />
          </Get>
          
          <Get Msg="TCAP::LCancelIndication">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" Status="Unsucc" />
            <Do Action="End" />
          </Get>

          <Get CallBack="CORRELATOR_END" Parameter="var::LocalCorrelator">
            <Do Trace="CORRELATOR RECEIVED {1}" Param1="var::LocalCorrelator" />
          </Get>
        </Gets>
      </State>

      <State Name="HardLimit">
        <OnState>
          <Do Trace="HARD LIMIT REACHED. NEW CALL IS IMPOSSIBLE" />
          <Do CallBack="CORRELATOR_END" Parameter="var::LocalCorrelator" />
        </OnState>
        <Gets>
          <Get CallBack="CORRELATOR_END" Parameter="var::LocalCorrelator">
            <Do Trace="CORRELATOR RECEIVED {1}" Param1="var::LocalCorrelator" />
          </Get>
        </Gets>
      </State>

      <State Name="Continue">
        <OnState>
          <Do Timer="PA::CallTime" /> <!-- CALL TIME IN SECONDS --> <!-- TraceTime="10" -->
        </OnState>
        <OnTimer>
          <Do Send="CAP::ApplyChargingReportCALL" CallActive="0" InvokeId="1" />
          <Do Send="TCAP::ContinueRequest" />
          <Do Send="CAP::EventReportCALL" InvokeId="2" EventType="const::Event_Disconnect" MessageType="var::DisconnectMessageType"/>          
          <Do Send="TCAP::ContinueRequest" />
        </OnTimer>
        <Gets>
          <Get Msg="CAP::ConnectCALL">
            <Do Send="CAP::EventReportCALL" EventType="const::Event_Answer" />
            <Do Send="TCAP::ContinueRequest" />
          </Get>
          <Get Msg="CAP::ContinueCALL">
            <Do Send="CAP::EventReportCALL" EventType="const::CALL_EventType_Answer" MessageType="var::AnswerMessageType"/>
            <Do Send="TCAP::ContinueRequest" />
          </Get>
          <Get Msg="CAP::ReleaseCALL" Cause="16">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" />
            <Do Action="End" />
          </Get>
          <Get Msg="CAP::ReleaseCALL" Cause="31">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" />
            <Do Action="End" />
          </Get>
          <Get Msg="CAP::ReleaseCALL">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" Status="Unsucc" />
            <Do Action="End" />
          </Get>

          <Get Msg="TCAP::ContinueIndication">
          </Get>
          
          <Get Msg="TCAP::LCancelIndication">
            <Do Action="TCAP::EndDialogue" />
            <Do Action="PA::CallEnd" Status="Unsucc" />
            <Do Action="End" />
          </Get>
          
          <Get Msg="TCAP::EndIndication">
          </Get>

          <Get Msg="CAP::ApplyChargingCALL">
            <Do Send="CAP::ApplyChargingReportCALL" CallActive="0" InvokeId="1" />
            <Do Send="TCAP::ContinueRequest" />
          </Get>
        </Gets>
      </State>
    </Scenario>



## Janova MMTP-терминал (2008)
Кроссплатформенный GUI-терминал для управления модулями оборудования сети мобильной связи компании Sitronics. Для внутреннего использования в компании.
Здесь я разрабатывал архитектуру, внешний дизайн и написал часть кода.
- Java/Swing/SWT.
- Официально для Intertel/Sitronics.
- Разработка в группе.

![9748_800](https://user-images.githubusercontent.com/53271533/230759227-409f2c34-981b-4e77-adc6-0a211ffa12be.jpg)

![10134_900](https://user-images.githubusercontent.com/53271533/230759173-9c581242-2a73-4d21-982b-1b2f6328170c.jpg)

Вариант внешнего дизайна.

![Image1](https://user-images.githubusercontent.com/53271533/230766903-2106fb32-661f-48fb-9262-43a42c33f918.jpg)

## STGM - Генератор SCCP-трафика (2008)
- Java/SWT/JNI/C++.
- Официально для Sitronics.
- Разработка в паре.

![8358_800](https://user-images.githubusercontent.com/53271533/230759219-380f174f-2e6c-4492-8500-8e3de8d6affc.jpg)

![8602_900](https://user-images.githubusercontent.com/53271533/230759220-c604d034-0031-4066-9ed6-cffdeb4e5ba2.jpg)

## Profiler Monitor (2007)
GUI-монитор профайлера производительности. Показывает время выполнения разных частей кода на уровне ядра и пользователя.
- Delphi.
- Неофициально для Intertel.
- Автор и единственный разработчик.

![8003_800](https://user-images.githubusercontent.com/53271533/230759215-a1b473d5-fc27-4e61-8261-ac062852a8c8.jpg)

## Bomber Monitor (2007)
Монитор одного из внутренних протоколов компании.
- С++/MFC.
- Неофициально для коллеги из Intertel.
- Автор и единственный разработчик.

![9540_800](https://user-images.githubusercontent.com/53271533/230759225-20b01b77-fa8c-49b4-8ea7-7188d2420292.jpg)

## Activity Checker (2006)
Утилита для контроля доступности физических модулей оборудования Sitronics. 
Программа использует обычный протокол пингования и может использования для контроля любых IP-узлов, поддерживающих пингование. Состояние модулей показано в виде таблицы. При изменении состояния пользователь видит всплывающие сообщения об этом.
Использование этой утилиты в рабочих процессах позволило случайно обнаружить и устранить скрытую пробему, при которой один из модулей системы перезагружался при падении другого модуля.
- Delphi.
- Неофициально для Intertel/Sitronics.
- Автор и единственный разработчик.

![3366_800](https://user-images.githubusercontent.com/53271533/230759196-738dddef-1da5-41af-a8fb-f70b429d9165.jpg)

![3988_900](https://user-images.githubusercontent.com/53271533/230759198-7d3d2b22-633a-48d4-9a92-fafefc4aaf6f.jpg)

![3637_900](https://user-images.githubusercontent.com/53271533/230759197-33805509-ef00-42c5-8386-6a82b4069019.jpg)

## Nasca Vision (2006)
Программа для визуализации и анализа логов внутреннего трафика сообщений между модулями ПО компании Strom Telecom/Sitronics. Основная функция - преобразование текстового лога сообщений в UML-диаграмму потока сообщений.
- Delphi.
- Неофициально для Intertel.
- Автор и единственный разработчик.

Общий вид программы и сгенерированная UML-диаграмма.

![4404_800](https://user-images.githubusercontent.com/53271533/230759200-04b4cb6b-f252-422d-accd-bc06fb401fdd.jpg)

Пример документации для разработчиков. Одна из функций программы - генерация схожей UML-диаграммы из текстового лога.

![4671_800](https://user-images.githubusercontent.com/53271533/230759201-73442638-c6f4-4426-a1b5-4d2584def939.jpg)

Функция синхронизации двух программ позволяет сравнивать два лога посредством синхронного скроллинга. При скроллинге одной из программ другая скроллится автоматически.

![5072_800](https://user-images.githubusercontent.com/53271533/230759202-2959cdfd-d3e5-48b4-9316-72d4635d0358.jpg)

Текстовое представление лога может статически и динамически подсвечиваться для более удобного анализа.

![5356_800](https://user-images.githubusercontent.com/53271533/230759203-abd399d2-b798-452d-a3bc-2e54f5eed2f5.jpg)

Доступна навигация между графическим и текстовым представлением лога. Также есть функция пометки нужных сообщений маркерами.

![5621_800](https://user-images.githubusercontent.com/53271533/230759204-3ffc99d1-f9c6-4ffb-86b6-848401db3c35.jpg)

Поддерживается интерфейс плагинов для других разработчиков.

![5639_800](https://user-images.githubusercontent.com/53271533/230759205-2513cb83-3c51-47f0-ab77-5fe48fc0d4a0.jpg)

Встроенная система поиска по текстовому логу с различными режимами фильтрации.

![5936_800](https://user-images.githubusercontent.com/53271533/230759206-6341ce4b-30f2-4ea1-867e-d0b001a87bed.jpg)

Кроме графического представления есть функция текстового представления структуры сообщений.

![6281_800](https://user-images.githubusercontent.com/53271533/230759207-74cd3c11-0cf6-4953-ae38-b917ab882085.jpg)

![6674_800](https://user-images.githubusercontent.com/53271533/230759209-ee068b8e-85f4-4e6f-8204-0d0e7147e215.jpg)

Встроенная база данных логов позволяет хранить, описывать и искать нужные логи.

![6402_800](https://user-images.githubusercontent.com/53271533/230759208-8c117bee-f880-4a09-8a05-0644d6519866.jpg)

Редактор описания формата сообщений включен в программу.

![7027_800](https://user-images.githubusercontent.com/53271533/230759210-042a73a3-9c2f-4a47-a5fe-0c33af41246d.jpg)

![4348_900](https://user-images.githubusercontent.com/53271533/230759199-8d3106dd-e54f-4e04-98f9-ebe817b97baa.jpg)

## MCGM - Монитор ресурсов и состояний генератора мобильного трафика MCG (2006)
GUI-монитор для генератора трафика MCG. Представляет собой легкий клиент, который получает все данные для построения GUI и отображения состояний и ресурсов от сервера (MCG). Таким образом этот монитор не требует каких-либо изменений при изменении списка ресурсов, которые нужно отображать. С момента своего создания в 2006 году он ни разу не менялся.
- Delphi.
- Неофициально для Intertel. Внедрен в рабочие процессы.
- Автор и единственный разработчик.

![7478_800](https://user-images.githubusercontent.com/53271533/230759212-2564d52c-5baa-4519-9da7-4c991c06734b.jpg)

![7760_900](https://user-images.githubusercontent.com/53271533/230759214-65d0f3fa-ec67-42bf-b54c-42c55332afdd.jpg)

## Fidel (2003)
Библиотека для обработки данных о длительности телефонных разговоров из файлов различных форматов. Библиотека включает в себя собственную реализация языка описания формата файла данных FDL (Fields Definition Language) и упрощенную реализацию языка SQL для написания запросов и получения нужной выборки из файлов. Реализация SQL также включает в себя математический процессор для написания математических выражений в теле SQL-запросов.
- С/С++.
- Проект написан в рамках дипломной работы в университете СибГУТИ.

### GUI-приложение, использующее библиотеку Fidel.
- Visual Basic

![1201_800](https://user-images.githubusercontent.com/53271533/230759184-17729137-8189-4da5-aa7a-f342598c4230.jpg)

![1373_800](https://user-images.githubusercontent.com/53271533/230759186-c606f585-6b96-4c46-8e60-27ffdf599b93.jpg)

### Еще одно GUI-приложения для демонстрации расчета часа наибольшей нагрузки. 
![1653_800](https://user-images.githubusercontent.com/53271533/230759187-c33ec6c7-61e4-409a-b6d2-560f49d7bfc2.jpg)
- Visual Basic

## Шифрование данных (2002)
Программа лабораторной работы для обучения студентов СибГУТИ работе российского стандарта шифрования данных. Интерактивное приложение, показывающее этапы шифрования данных с анимацией.
- Delphi.
- Официально для СибГУТИ.

![2715_900](https://user-images.githubusercontent.com/53271533/230759192-32b359d6-2c92-4a3e-affe-df551ad77a17.jpg)

![3140_800](https://user-images.githubusercontent.com/53271533/230759194-591b742e-3af7-49c6-98c6-a0f9cdde0caa.jpg)

![2899_900](https://user-images.githubusercontent.com/53271533/230759193-03a8a4b4-9ccb-42d4-8b6c-ccdaa69cacc0.jpg)

## Диспетчирование вызовов (2001)
Программа лабораторной работы для обучения студентов СибГУТИ процессу диспетчирования программ обслуживания вызовов в цифровых телефонных станциях.
- Delphi
- Официально для СибГУТИ.
-  
![1910_900](https://user-images.githubusercontent.com/53271533/230759188-1b2a7f99-425b-4627-ace3-8729815325a9.jpg)

![2216_800](https://user-images.githubusercontent.com/53271533/230759189-39e8a260-3860-4001-9803-27e82e825c9f.jpg)

![2305_800](https://user-images.githubusercontent.com/53271533/230759191-3aedb171-e681-451b-86d0-06b5b4747248.jpg)


