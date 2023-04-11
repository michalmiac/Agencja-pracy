# Agencja-pracy

+ [Klastr sieciowy](https://github.com/michalmiac/Agencja-pracy/edit/main/README.md#se%C4%87-komputerowa)
+ [Rozwiązania techniczne VoIP](https://github.com/michalmiac/Agencja-pracy/edit/main/README.md#rozwi%C4%85zania-techniczne-voip)
+ [Oprogramowanie do obsługi biura](https://github.com/michalmiac/Agencja-pracy/edit/main/README.md#oprogramowanie-do-obs%C5%82ugi-biura)


W mojej agencji pracy, która zajmuje się zatrudnianiem pracowników do opieki osób starszych w ich własnych domach, dziedzina informatyczna odgrywa kluczową rolę. W oparciu o specjalistyczne oprogramowanie, rozwijane przeze mnie, byliśmy w stanie efektywnie zarządzać i organizować pracę naszych pracowników oraz zapewnić pełną obsługę administracyjną biura.

Moje rozwiązania informatyczne pozwalają na łatwe i szybkie zarządzanie zleceniami, przypisywanie opiekunów do konkretnych klientów, monitorowanie realizacji zadań oraz generowanie raportów. Wszystkie te funkcjonalności są dostępne w przejrzystym i intuicyjnym interfejsie graficznym, który został zaprojektowany z myślą o wygodzie i efektywności pracy moich pracowników.

Oprócz rozwiązań związanych bezpośrednio z zarządzaniem zleceniami, oprogramowanie zawiera również specjalne narzędzia dla działu rekrutacji, które pozwalają na szybkie i precyzyjne przeprowadzenie procesu rekrutacji oraz prowadzenie pełnej dokumentacji pracowników.

Wszystkie te rozwiązania informatyczne są stale rozwijane i doskonalone przeze mnie, aby sprostać wymaganiom naszych klientów oraz zapewnić najlepszą jakość usług w dziedzinie opieki nad osobami starszymi.


# Klastr sieciowy
![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/20230407_174626.jpg)
Przedstawione zdjęcie ukazuje klastr sieciowy w fazie testowej. Po lewej stronie znajdują się serwery, które działają jako serwery plików, backupy, bazy danych oraz backendy aplikacji do zarządzania biurem. Na prawo i na dole widoczne są routery WiFi, switch oraz router Cisco. Wszystkie urządzenia w biurze, łącznie z komputerami, drukarkami i urządzeniami monitorującymi, są podłączone do centralnego punktu, który oddziela i zabezpiecza połączenia, zapewniając odpowiednią przepustowość potrzebną do najefektywniejszej pracy złożonej infrastruktury.

+ Instalacja obrazu systemu **Ubuntu Server** na urządzeniu **Raspberry**, jako stabilnego i dobrze znanej mi struktury systemu.
  + Zastosowanie bazy danych **MongoDB**, ze względu na format **JSON**, dla agregacji obiektów z języka Java
  + **SpringBoot** wykorzystany jako REST server
  + Dostęp do serwera plików za pomocą protokołu **SSH**. Zewnętrzny graficzny dostęp do plików za pośrednictwem protokołu **SFTP** w oknie eksploratora plików w       systemie Ubuntu.
  + Program **Bacula** do tworzenia kopii zapasaowych
  + Dostęp zdalny do zasobów za pomocą technologii **OpenVPN**


# Rozwiązania techniczne VoIP
![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/20230407_164237.jpg)
Na powyższym zdjęciu widoczne są elementy elektroniczne ułożone kolejno od lewej strony: przetwornica step-down, moduł GSM/GPRS SIM800L, złącza wychodzące z modułu do płytki z rezystorami, które prowadzą do połączenia Audio Jack, oraz na końcu karta dźwiękowa. Dzięki połączeniu modułu SIM800L z komputerem za pomocą portu szeregowego, możliwe jest sterowanie modułu, wysyłanie poleceń służących do wysyłania i odbierania wiadomości tekstowych (SMS) oraz  wydawania poleceń do rozpoczęcia połączeń głosowych. Do tego projektu specjalnie stworzono program w języku Java umożliwiający wysyłanie poleceń ATM przez port szeregowy do płytki GSM, a tym samym odbieranie i wysyłanie wiadomości tekstowych (SMS) przez ten sam kanał. Natomiast dźwięk, który dociera do modułu GSM, jest przekazywany przez rezystory do złącza Audio Jack, a następnie do karty dźwiękowej. Wysyłanie dźwięku do modułu GSM działa w dokładnie odwrotny sposób, gdzie karta graficzna wysyła dźwięk do złącza Audio Jack, a następnie przechodzi on przez rezystory do płytki GSM, co pozwala na wymianę dźwiękową. Istotnym elementem w przedstawionym połączeniu dźwiękowym jest przesyłanie poleceń ATM w celu rozpoczęcia połączenia, ale oczywiście równie ważne jest możliwość odbierania dźwięku oraz wysyłania dźwięku z karty graficznej. Do tego celu służył kolejny program napisany w języku Java. 

# Oprogramowanie do obsługi biura
### Poniżej przedstawiono graficzne ujęcia niektórych modułów programu do zarządzania zadaniami w biurze. Stanowią one jedynie niewielki wycinek dostępnych funkcjonalności, a ich celem jest ogólne zobrazowanie zadań, które stoją przed naszą firmą.

![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2015-44-34.png)

Powyżej przedstawiono ekran powitalny programu. Pracownik może zdecydować, czy chce się zalogować do systemu. W zależności od lokalizacji użytkownika, program oferuje wybór typu połączenia z bazą danych.


![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2012-51-18.png)
Na pierwszym zdjęciu, które jest widoczne po zalogowaniu się użytkownika, pojawia się interfejs graficzny umożliwiający dodawanie, usuwanie oraz wyświetlanie pracowników z baz kontaktowych. Centralnym elementem interfejsu jest tabela prezentująca listę kontaktów, która umożliwia filtrowanie i sortowanie wyników według różnych kryteriów, takich jak znajomość języka czy płeć. Takie funkcjonalności są niezwykle istotne dla firmy, ponieważ umożliwiają odnajdywanie pracowników, którzy są idealnie dopasowani do potrzeb klientów, takich jak starsze osoby wymagające opieki. Baza danych pracowników, która została ujęta w interfejsie graficznym, stanowi zatem najważniejszy zasób firmy.


![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2014-15-04.png)
Na tym zdjęciu ukazane jest okno, które służy do zapisywania danych kontaktowych pracownika w bazie danych. Opcje, które można wybrać podczas zapisywania informacji, są niezwykle istotne z punktu widzenia rekrutacji, umożliwiając dokładną ocenę spełnienia wymagań klienta przez danego pracownika. Przykładowo, można określić preferencje dotyczące palenia papierosów. Dodatkowo, korzyścią jest możliwość zapisywania rozmów z pracownikiem, co zapewnia przyszłą możliwość odnalezienia niezbędnych informacji z rozmów. Dzięki temu okno zapisywania kontaktów stanowi wyjątkowo przydatne narzędzie dla firmy, pozwalając na dokładne dobieranie pracowników do potrzeb klientów.



![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2012-53-26.png)
W kolejnym oknie prezentowany jest moduł służący do wyliczania wynagrodzeń dla pracowników. To narzędzie ma na celu ułatwienie procesu wyliczania wynagrodzeń i zapobieganie błędom, które mogą wystąpić przy manualnym obliczaniu płac. Proces ten jest bardzo skomplikowany i wymaga uwzględnienia różnych aspektów, takich jak dokładna godzina rozpoczęcia pracy, waluta wypłacanego wynagrodzenia, odliczenia za transport czy komornika, a także przeliczanie tych należności na różne waluty. Dużą zaletą tego modułu jest możliwość generowania wyliczeń w formie protokołu PDF, co umożliwia przesłanie ich pracownikom, aby mogli dokładnie zapoznać się z każdym krokiem wyliczenia swojego wynagrodzenia.



![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2012-53-47.png)
Kolejne okno prezentuje moduł służący do przypisywania i śledzenia zadań powierzonych pracownikom biurowym. Jest to niezwykle istotne narzędzie, ponieważ pozwala nie tylko na przypisanie zadania konkretnemu pracownikowi, ale także na śledzenie etapów jego wykonania. Każdy pracownik ma możliwość monitorowania zadań przypisanych do niego oraz zapisywania niezbędnych informacji dotyczących ich wykonania. Dzięki temu modułowi praca w biurze staje się bardziej efektywna i zorganizowana, a pracownicy mogą skuteczniej realizować powierzone im zadania.

![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2012-54-12.png)
Na zdjęciu przedstawiony jest moduł, który umożliwia tworzenie kwestionariusza osobowego dla pracowników do opieki. Dzięki temu narzędziu można w łatwy sposób zbierać i gromadzić istotne informacje dotyczące naszych pracowników. Warto podkreślić, że wygenerowany w ten sposób formularz może być wyeksportowany do formatu PDF, co pozwala na łatwe przesłanie go w późniejszym etapie rekrutacji do naszych klientów. Dzięki temu nasi klienci mogą zapoznać się z wstępnymi informacjami na temat potencjalnego opiekuna i dokonać wyboru najlepszego kandydata do ich opieki.

![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2012-55-02.png)
Powyżej przedstawiony moduł umożliwia wyszukiwanie transportów służących do przewozu naszych pracowników do miejsca pracy. Ze względu na fakt, że nasi pracownicy zamieszkują praktycznie wszystkie obszary Polski, prowadzona jest baza danych przewoźników uwzględniająca obszary, które obsługują w ramach swoich usług transportowych. Dzięki takiemu narzędziu możliwe jest istotne skrócenie czasu poszukiwań przewoźników w porównaniu do tradycyjnej metody dzwonienia do każdego z nich.

![My animated logo](https://github.com/michalmiac/Agencja-pracy/blob/main/graphics/Screenshot%20from%202023-04-07%2015-15-16.png)
W tym ujęciu przedstawiony jest moduł odpowiedzialny za przechowywanie dokumentów, zleceń oraz informacji zebranych z całego programu zatrudnionych pracowników. Dzięki temu modułowi możemy automatycznie generować dokumenty w formacie PDF, takie jak umowy, zlecenia podróży, ewidencję czasu pracy oraz różnego rodzaju raporty. Istnieje możliwość śledzenia, gdzie dokładnie znajdują się dokumenty w danym momencie po ich wysłaniu do pracownika, na przykład przez tradycyjną pocztę. Jednym z ważnych elementów tego modułu jest możliwość przeglądania informacji na temat dokumentów, które wymagają opracowania, uzupełnienia, złożenia lub wysłania. Moduł "informacje" stanowi centralne miejsce gromadzenia danych z całego programu dotyczących rzeczy, które są jeszcze do należy podjąć w odniesieniu dla danego pracownika.


### Poniżej przedstawione zostały fragmenty kodu oprogramowania, które służą do obsługi zadań biurowych i mają na celu pokazanie technicznych rozwiązań zastosowanych w aplikacji. Przedstawione kod zostały zaprojektowany z myślą o zwiększeniu efektywności programowania oraz zapewnieniu większej wydajności i skalowalności aplikacji. Dzięki nim tworzenie aplikacji staje się bardziej intuicyjne, a programowanie jest łatwiejsze i szybsze.

<pre><code> default Object createDto(Object dtoObject, Object controllerClass, @Nullable List<?> list, @Nullable String ARRAY_NAME) throws IOException {
    ObjectMapper mapper = new ObjectMapper();
    ObjectNode jsonNode = mapper.createObjectNode();

    for (Field field : controllerClass.getClass().getDeclaredFields()) {
        if (field.isAnnotationPresent(MyAnno.class)) {
            field.setAccessible(true);
            try {
                Object value = field.get(controllerClass);

                if (value == null) {
                    jsonNode.putNull(field.getName());
                } else {
                    switch (field.getType().getCanonicalName()) {
                        case "javafx.scene.control.TextField":
                            jsonNode.put(field.getName(), ((TextField) value).getText());
                            break;
                        case "javafx.scene.control.DatePicker":
                            LocalDate dateValue = ((DatePicker) value).getValue();
                            jsonNode.put(field.getName(), dateValue != null ? dateValue.toString() : null);
                            break;
                        case "javafx.scene.control.ChoiceBox":
                            jsonNode.put(field.getName(), ((ChoiceBox<?>) value).getValue().toString());
                            break;
                        case "javafx.scene.control.CheckBox":
                            jsonNode.put(field.getName(), ((CheckBox) value).isSelected());
                            break;
                        case "javafx.scene.control.TextArea":
                            jsonNode.put(field.getName(), ((TextArea) value).getText());
                            break;
                        case "java.lang.String":
                            jsonNode.put(field.getName(), (String) value);
                            break;
                        case "java.util.Optional":
                            Optional<?> optional = (Optional<?>) value;
                            if (optional.isPresent()) {
                                jsonNode.put(field.getName(), optional.get().toString());
                            } else {
                                jsonNode.putNull(field.getName());
                            }
                            break;
                        default:
                            throw new IllegalArgumentException("Unsupported field type: " + field.getType().getCanonicalName());
                    }
                }
            } catch (IllegalAccessException e) {
                e.printStackTrace();
            }
        }
    }

    if (list != null && !list.isEmpty()) {
        ArrayNode arrayNode = mapper.createArrayNode();
        for (Object scheduleInfoDto : list) {
            String scheduleInfoJson = mapper.writeValueAsString(scheduleInfoDto);
            arrayNode.add(mapper.readTree(scheduleInfoJson));
        }
        jsonNode.set(ARRAY_NAME, arrayNode);
    }

    dtoObject = mapper.treeToValue(jsonNode, dtoObject.getClass());
    return dtoObject;
}
    </code></pre>
    
Ten kod ma na celu umożliwienie skalowalności poprzez wykorzystanie adnotacji MyAnno, która pozwala swobodnie określać pola, z których ma być wyciągnięta wartość. Dzięki temu można w łatwy sposób dodać nowe pola bez konieczności modyfikowania metody createDto.
    
+ Użyłem obiektu ObjectNode do przechowywania kluczy i wartości w formacie JSON.
+ Ustawiłem dostępność prywatnych pól poprzez użycie field.setAccessible(true).
+ Dodałem dodatkowe sprawdzenie dla wartości null, aby uniknąć wyjątków.
+ Użyłem wyrażenia switch z jawnymi wartościami dla typów pól, co pozwala uniknąć konieczności korzystania z metody instanceof.
+ Dodatkowo obsłużyłem typ Optional, dzięki czemu można bezpiecznie używać pola, które może być nullem lub zawierać wartość opakowaną w Optional.



     <code><pre> default void setEventHandlerOnAllElements(Object controllerClass, EventHandleInterfaceHandler eventHandleInterfaceHandler, ButtonEventHandleInterfaceHandler buttonEventHandleInterfaceHandler)  {
        Arrays.stream(controllerClass.getClass().getFields()).filter(fieldAll -> fieldAll.isAnnotationPresent(MyAnno.class)).forEach(fieldFiltered -> {
            switch (fieldFiltered.getType().getCanonicalName()) {
                case "javafx.scene.control.Button":
                    Button button = null;
                    try {
                        button = (Button) fieldFiltered.get(controllerClass);
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                    button.setOnAction(new EventHandler<ActionEvent>() {
                        @Override
                        public void handle(ActionEvent event) {
                            buttonEventHandleInterfaceHandler.handle();
                        }
                    });
                    break;
                case "javafx.scene.control.CheckBox":
                    CheckBox checkBox = null;
                    try {
                        checkBox = (CheckBox) fieldFiltered.get(controllerClass);
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                    checkBox.setOnAction(new EventHandler<ActionEvent>() {
                        @SneakyThrows
                        @Override
                        public void handle(ActionEvent event) {
                            eventHandleInterfaceHandler.handle();
                        }
                    });
                    break;
                case "javafx.scene.control.ChoiceBox":
                    ChoiceBox choiceBox = null;
                    try {
                        choiceBox = (ChoiceBox) fieldFiltered.get(controllerClass);
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                    choiceBox.setOnAction(new EventHandler<ActionEvent>() {
                        @SneakyThrows
                        @Override
                        public void handle(ActionEvent event) {
                            eventHandleInterfaceHandler.handle();
                        }
                    });
                    break;
            }

        });


    }
    
        </code></pre>


Powyższy kod mać na celu ułatwienie obsługi zdarzeń dla wielu elementów interfejsu użytkownika w kontrolerze w JavaFX. Adnotacja MyAnno została stworzona specjalnie do tego celu i służy do oznaczania pól w klasie kontrolera, które mają być użyte do obsługi zdarzeń. Zgodnie z kodem, tylko pola oznaczone tą adnotacją będą przetwarzane w metodzie setEventHandlerOnAllElements.
To podejście może ułatwić programowanie interfejsu użytkownika, gdyż pozwala na zdefiniowanie pól, które mają być użyte do obsługi zdarzeń, a następnie ich szybkie i łatwe przetwarzanie w całej klasie kontrolera.


