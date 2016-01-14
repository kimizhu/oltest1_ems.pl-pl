---
description: na
keywords: na
title: FastTrack Center Benefit Process for Azure Rights Management
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d85708b-a837-4865-aef9-0dd4488b23e9
---
# Proces asysty centrum rozwiązania FastTrack dla usługi Azure Rights Management
Jeśli Twoja organizacja jest uprawniona do asysty centrum rozwiązania FastTrack dla usługi Microsoft Azure Rights Management, możesz podjąć zdalną współpracę ze specjalistami firmy Microsoft w celu przygotowania swojego środowiska usługi Azure RMS do użycia. Aby dowiedzieć się, czy Twoja organizacja jest uprawniona, zobacz [Asysta centrum rozwiązania FastTrack dla usługi Azure Rights Management](../Topic/FastTrack_Center_Benefit_for_Azure_Rights_Management.md).

Ten artykuł zawiera następujące informacje:

-   [Overview of the onboarding process](#overview_rms)

-   [Expectations for your source environment](#expectations_src_environ_rms)

-   [Phases of the onboarding process](#phases_onboarding_process_rms)

-   [Microsoft responsibilities](#microsoft_responsibilities_rms) — dla każdej fazy

-   [Your responsibilities](#your_responsibilities_rms) — dla każdej fazy

Czego można oczekiwać po zakończeniu dołączania:

-   Dzierżawca usługi Microsoft Azure RMS będzie utworzony.

-   Licencjonowani użytkownicy będą mieli dostęp do usług Azure RMS za pomocą jednej z następujących opcji tożsamości:

    -   Tożsamości w chmurze (unikatowe konta usługi Microsoft Azure AD).

    -   Tożsamości synchronizowane: konta usługi Microsoft Azure AD synchronizowane z lokalną usługą Active Directory za pomocą narzędzia Azure Active Directory Connect (Azure AD Connect) w przypadku klientów z pojedynczym lasem lub wieloma lasami usługi Active Directory.

    -   Tożsamości federacyjne — z kontami usługi Microsoft Azure AD, które są:

        -   Synchronizowane z usługą Active Directory za pomocą narzędzia Microsoft Azure AD Connect w przypadku klientów używających konfiguracji z pojedynczym lasem usługi Active Directory.

        -   Federowane za pomocą usług Active Directory Federation Services (AD FS) 2.0 lub nowszych z lokalnej usługi Active Directory.

## <a name="overview_rms"></a>Omówienie procesu dołączania
Oto dwa istotne etapy procesu dołączania:

-   **Podstawowe możliwości** — zadania wymagane w celu skonfigurowania dzierżawy i zintegrowania z usługą Azure AD, jeśli to konieczne. Funkcje podstawowe stanowią też bazę do dołączenia do innych kwalifikujących się usług online firmy Microsoft.

-   **Dołączanie do usługi** — zadania wymagane do skonfigurowania autonomicznej usługi Azure RMS albo usługi korzystającej z synchronizacji z katalogiem za pomocą narzędzia Azure AD Connect bądź usług AD FS.

Na poniższym diagramie przedstawiono oś czasu asysty centrum rozwiązania FastTrack.

![](../Image/1-rms_onboarding_process.png)

Podstawowy proces przebiega w następujący sposób:

-   Firma Microsoft podejmie próbę skontaktowania się z Tobą w ciągu 30 dni od daty zakupu uprawniającego planu. Możesz również poprosić o pomoc z [centrum rozwiązania FastTrack](http://fasttrack.microsoft.com/), gdy wszystko będzie gotowe do wdrożenia tych usług w Twojej organizacji. Aby poprosić o pomoc, zaloguj się do centrum rozwiązania FastTrack (http://fasttrack.microsoft.com), przejdź do pulpitu nawigacyjnego, wybierz nazwę firmy, kliknij kartę Oferty i kliknij przycisk prośby o pomoc w ramach kwalifikującej się usługi.

-   Zespół firmy Microsoft pomoże Ci na etapie podstawowych możliwości, a następnie pomoże Ci dołączyć — jeden raz — do każdej z kwalifikujących się usług.

Pomoc techniczna dotycząca dołączania będzie świadczona w całości zdalnie przez przydzielony do tego personel firmy Microsoft:

-   Firma Microsoft będzie zdalnie pomagać Ci w różnych działaniach związanych z dołączaniem za pomocą narzędzi, dokumentacji i wskazówek. Jeśli chcesz, aby pracownicy firmy Microsoft wykonali za Ciebie niektóre zadania konfiguracyjne, możesz nadać firmie Microsoft prawa dostępu i inne uprawnienia niezbędne do realizacji tych zadań.

-   Pomoc techniczna dotycząca dołączania jest świadczona przez centrum programu FastTrack w normalnych godzinach pracy dla danego regionu.

-   Pomoc techniczna dotycząca dołączania jest dostępna w następujących językach: angielski, chiński (uproszczony), francuski, hiszpański, japoński, niemiecki, portugalski (Brazylia) i włoski.

-   Zespół firmy Microsoft może współpracować bezpośrednio z Tobą lub wyznaczonym przez Ciebie przedstawicielem.

## <a name="expectations_src_environ_rms"></a>Oczekiwania dotyczące środowiska źródłowego
W środowisku źródłowym może już istnieć lokalna usługa Microsoft Active Directory, którą chcesz zintegrować z usługą Microsoft Azure Active Directory, aby umożliwić rozbudowane zarządzanie tożsamościami z poziomu pojedynczej konsoli. Asysta centrum rozwiązania FastTrack obejmuje pomoc w integracji usługi Microsoft Azure Active Directory z istniejącą implementacją lokalną. Jeśli wymagana jest integracja, środowisko źródłowe musi działać co najmniej na poziomie minimalnym dla danego zastosowania.

W poniższej tabeli przedstawiono oczekiwania dotyczące istniejącego środowiska źródłowego związane z dołączaniem.

|Aktywność|Oczekiwania dotyczące środowiska źródłowego|
|-------------|-----------------------------------------------|
|Podstawowe możliwości|Lasy usługi Active Directory z ustawionym poziomem funkcjonalności lasu co najmniej systemu Windows Server 2008 i następującą konfiguracją lasów:<br /><br />-   Pojedynczy las usługi Active Directory<br />-   Wiele lasów usługi Active Directory **Note:** W przypadku wszystkich konfiguracji z wieloma lasami wdrożenie usług AD FS wykracza poza zakres asysty centrum rozwiązania FastTrack.|
|Etap dołączania do usługi<br /><br />-   Azure RMS|Lokalna usługa Active Directory i lokalne środowisko zostały przygotowane na potrzeby usługi Azure RMS, co obejmuje skorygowanie zidentyfikowanych problemów, które uniemożliwiłyby integrację z funkcjami usługi Azure AD i Azure RMS.|

## <a name="phases_onboarding_process_rms"></a>Fazy procesu dołączania
Dołączanie do usługi Azure RMS składa się z pięciu podstawowych faz, jak pokazano na poniższej ilustracji:

-   Inicjowanie

-   Ocena

-   Korygowanie

-   Włączenie

-   Zamknij

![](../Image/2-aadp_onboarding_phases-v3.png)

Aby poznać szczegóły zadań realizowanych w każdej fazie, zobacz sekcje [Microsoft responsibilities](#microsoft_responsibilities_rms) i [Your responsibilities](#your_responsibilities_rms).

### Faza inicjowania
Po zakupie odpowiedniej liczby licencji postępuj zgodnie ze wskazówkami z wiadomości e-mail z potwierdzeniem zakupu w celu skojarzenia licencji z istniejącym lub nowym dzierżawcą. Firma Microsoft zweryfikuje Twoje uprawnienia do asysty centrum rozwiązania FastTrack. Firma Microsoft podejmie próbę skontaktowania się z Tobą w ciągu 30 dni od daty zakupu uprawniającego planu. Możesz również poprosić o pomoc z [centrum rozwiązania FastTrack](http://fasttrack.microsoft.com/), gdy wszystko będzie gotowe do wdrożenia tych usług w Twojej organizacji. Aby poprosić o pomoc, zaloguj się do centrum rozwiązania FastTrack (http://fasttrack.microsoft.com), przejdź do pulpitu nawigacyjnego, wybierz nazwę firmy, kliknij kartę Oferty i kliknij przycisk prośby o pomoc w ramach kwalifikującej się usługi.

W tej fazie omówimy proces dołączania, zweryfikujemy dane i zorganizujemy spotkanie wstępne.

![](../Image/Microsoft_Azure_AD_Premium_initiate_phase_1.png)

### Faza oceny
Po rozpoczęciu procesu dołączania firma Microsoft we współpracy z Tobą oceni Twoje środowisko źródłowe i wymagania. Zostaną uruchomione narzędzia umożliwiające ocenę środowiska i firma Microsoft przeprowadzi Cię przez proces oceny lokalnej usługi Active Directory, przeglądarek internetowych, systemów operacyjnych na urządzeniach klienckich, usługi DNS, sieci, infrastruktury i systemu tożsamości w celu ustalenia, czy ze względu na dołączenie są wymagane zmiany. Na podstawie bieżącej konfiguracji udostępnimy plan korekt pozwalających zapewnić spełnienie przez środowisko źródłowe minimalnych wymagań na potrzeby pomyślnego dołączenia do usługi Azure RMS. Zaplanujemy też odpowiednie rozmowy kontrolne do przeprowadzenia w fazie korygowania.

![](../Image/Microsoft_Azure_AD_Premium_assess_phase_v6.png)

### Faza korygowania
Jeśli będzie to konieczne, wykonasz ustalone w planie korekt zadania w środowisku źródłowym, aby zapewnić spełnienie minimalnych wymagań na potrzeby dołączenia do poszczególnych usług.

![](../Image/Microsoft_Azure_AD_Premium_remediate_phase_1.png)

Przed rozpoczęciem fazy włączania wspólnie zweryfikujemy wyniki działań korygujących, aby upewnić się, że wszystko jest gotowe do kontynuacji.

### Faza włączania
Po ukończeniu wszystkich działań korygujących projekt przewiduje skonfigurowanie w infrastrukturze podstawowej korzystania z usług i zainicjowanie obsługi usługi Azure RMS.

**Faza włączania — podstawowe możliwości**

Włączanie podstawowych możliwości obejmuje zainicjowanie obsługi usług oraz zintegrowanie dzierżawy i tożsamości. Obejmuje też kroki utworzenia podstaw do dołączenia do usługi Microsoft Azure RMS.

Po zakończeniu etapu podstawowego dołączania można rozpocząć dołączanie do usługi Azure RMS.

**Faza włączania — Azure RMS**

W razie potrzeby środowisko usługi Azure RMS można skonfigurować pod kątem synchronizacji z katalogiem Azure AD Connect i usług Active Directory Federation Services (AD FS).

W przypadku scenariuszy Azure RMS obejmujących synchronizowanie tożsamości lokalnych z chmurą pomożemy Ci przez dodanie użytkowników i administratorów IT do Twojej subskrypcji, skonfigurowanie wymagań wstępnych zarządzania, skonfigurowanie usługi Azure RMS, skonfigurowanie synchronizacji katalogu i usług Active Directory Federation Services przy użyciu narzędzia Azure AD Connect, skonfigurowanie użytkowników testowych i walidację podstawowych zastosowań usługi.

Konfiguracja usługi Azure RMS obejmuje włączenie następujących funkcji:

-   Włączenie usługi RMS

-   Konfiguracja zarządzania prawami do informacji dla usługi Exchange Online i Sharepoint Online

-   Łącznik usługi Rights Management z lokalnym programem Exchange i Sharepoint

-   Aplikacja do tworzenia i przetwarzania dokumentów chronionych usługą RMS dla urządzeń z systemem Windows i innymi systemami

![](../Image/Microsoft_Azure_AD_Premium_enable_phase_2.png)

## <a name="microsoft_responsibilities_rms"></a>Obowiązki firmy Microsoft:

### Ogólne

-   Zapewnianie Ci zdalnej pomocy technicznej w zakresie wymaganych działań konfiguracyjnych zgodnie z informacjami podanymi w szczegółowych opisach faz.

-   Zapewnianie dostępnej dokumentacji i narzędzi programowych, konsol administracyjnych i skryptów ułatwiających ograniczenie lub wyeliminowanie zadań konfiguracji.

Nadanie firmie Microsoft praw dostępu i innych uprawnień nie jest wymagane, aby skorzystać z asysty centrum rozwiązania FastTrack. W niektórych przypadkach możesz podjąć decyzję o nadaniu firmie Microsoft praw dostępu i innych uprawnień w celu wykonania określonych działań w Twoim imieniu.

### Faza inicjowania

-   Skontaktowanie się z Tobą w ciągu 30 dni od zakupu uprawniających licencji dla nowej dzierżawy.

-   Zdefiniowanie kwalifikujących się usług, do których chcesz dołączyć.

### Faza oceny

-   Zapewnianie przeglądu administracyjnego.

-   Zapewnianie wskazówek w następującym zakresie:

    -   Wymagania związane z usługą DNS, siecią i infrastrukturą.

    -   Wymagania związane z klientami (przeglądarka internetowa, kliencki system operacyjny i potrzeby związane z usługami).

    -   Inicjowanie obsługi i tożsamości użytkowników.

    -   Identyfikacja wymagań synchronizacji katalogu.

    -   Włączanie kwalifikujących się usług, które zostały zakupione i zdefiniowane jako część procesu dołączania.

    -   Identyfikacja wymagań środowiska pilotażowego i testowego, które należy spełnić.

-   Ustalenie osi czasu działań korygujących.

-   Udostępnienie listy korekt.

### Faza korygowania

-   Prowadzenie z Tobą rozmów konferencyjnych zgodnie z ustalonym harmonogramem w celu monitorowania postępu działań korygujących.

-   Pomoc przy korzystaniu z narzędzi identyfikujących i korygujących problemy oraz przy interpretowaniu wyników.

### Faza włączania
Zapewnianie wskazówek w następującym zakresie:

-   Aktywowanie dzierżawcy usługi Azure RMS.

-   Konfigurowanie portów zapory.

-   Konfigurowanie usługi DNS dla kwalifikujących się usług.

-   Walidacja łączności z usługami Azure RMS.

-   W przypadku środowiska z jednym lasem:

    -   Wdrażanie synchronizacji katalogu między Usługami domenowymi Active Directory a narzędziem Azure AD Connect, jeśli jest to wymagane.

    -   Konfigurowanie synchronizacji haseł za pomocą narzędzia Azure AD Connect.

-   W przypadku środowiska z wieloma lasami:

    -   Wdrażanie synchronizacji za pomocą narzędzia Azure AD Connect skonfigurowanej na potrzeby scenariuszy z wieloma lasami. Pamiętaj, że funkcje synchronizacji skrótów haseł i zapisywania zwrotnego haseł obsługują wiele lasów.  Jednak inne scenariusze zapisywania zwrotnego nie są obsługiwane.

    -   Konfigurowanie synchronizacji między lokalnymi lasami usługi Active Directory a katalogiem usługi Microsoft Azure AD (Azure Active Directory).

        > [!NOTE]
        > Projektowanie i wdrażanie rozwiązań niestandardowych rozszerzeń reguł wykracza poza zakres tej asysty.

-   W przypadku pojedynczego lasu, gdy obiektem docelowym są tożsamości federacyjne: instalowanie i konfigurowanie usług Active Directory Federation Services (AD FS) na potrzeby uwierzytelniania domeny lokalnej za pomocą usługi Microsoft Azure AD w odpornej na uszkodzenia konfiguracji pojedynczej lokacji, jeśli jest to wymagane.

    > [!NOTE]
    > W przypadku wszystkich konfiguracji z wieloma lasami wdrożenia usług AD FS wykraczają poza zakres tej asysty.

-   Testowanie funkcji logowania jednokrotnego, jeśli ją wdrożono.

-   Dodawanie kolejnych administratorów zabezpieczeń informacji w celu zarządzania szablonami.

-   Przypisywanie konta administratora do usługi Azure RMS.

-   Licencjonowanie dwóch użytkowników pilotażowych usługi Azure RMS.

-   Konfigurowanie dwóch testowych grup dystrybucji w celu walidacji zasad.

-   Konfigurowanie jednego szablonu niestandardowego usługi Azure RMS na potrzeby katalogu.

-   Zapewnianie wskazówek dotyczących konfigurowania integracji usług SharePoint Online i Exchange Online z usługą Azure RMS, w tym:

    -   Konfigurowanie i walidacja integracji usługi Exchange Online z usługą Azure RMS.

    -   Konfigurowanie jednej testowej reguły przepływu poczty szyfrującej poufne wiadomości wysyłane do adresatów spoza Twojej organizacji.

    -   Konfigurowanie i walidacja ochrony usługi SharePoint Online dla jednej biblioteki testowej, która ma być chroniona przez usługę Azure RMS.

-   Konfigurowanie łącznika usługi RMS na jednym serwerze lokalnym, jeśli jest to wymagane:

    -   Konfigurowanie i walidacja integracji lokalnego programu Exchange 2013/2010 z usługą Azure RMS.

    -   Konfigurowanie przy użyciu łącznika jednej testowej reguły przepływu poczty szyfrującej poufne wiadomości wysyłane do adresatów spoza Twojej organizacji.

    -   Konfigurowanie i walidacja ochrony lokalnego programu SharePoint 2013/2010 dla jednej biblioteki testowej, która ma być chroniona przez usługę Azure RMS.

-   Konfigurowanie aplikacji do tworzenia i przetwarzania dokumentów chronionych usługą RMS dla urządzeń z systemem Windows i innymi systemami.

## <a name="your_responsibilities_rms"></a>Twoje obowiązki
W tej sekcji opisano niektóre z Twoich obowiązków podczas procesu dołączania.

### Ogólne

-   Wprowadzanie wszelkich ulepszeń i integracji w dzierżawcy usługi Azure RMS, które wykraczają poza konfigurowalne opcje wymienione w tym artykule.

-   Ogólne zarządzanie programem i projektami w zakresie Twoich zasobów.

-   Komunikowanie się z użytkownikami końcowymi, przygotowywanie dokumentacji i szkoleń oraz zarządzanie zmianami.

-   Dokumentacja pomocy dla użytkowników i szkolenia.

-   Tworzenie wszelkich raportów, prezentacji lub protokołów spotkań specyficznych dla Twojej organizacji.

-   Tworzenie dokumentacji dotyczącej architektury i technicznej specyficznej dla Twojej organizacji.

-   Projektowanie, nabywanie, instalowanie i konfigurowanie sprzętu oraz sieci.

-   Nabywanie, instalowanie i konfigurowanie oprogramowania.

-   Konfigurowanie i stosowanie zasad zabezpieczeń innych niż utworzone na potrzeby testowania konfiguracji i funkcjonalności podstawowej usług Azure RMS oraz zarządzanie tymi zasadami.

-   Rejestrowanie kont użytkowników innych niż te wykorzystywane do testowania konfiguracji i funkcjonalności podstawowej usług Azure RMS.

-   Analiza, weryfikowanie przepustowości, testowanie, monitorowanie i konfigurowanie sieci.

-   Zarządzanie procesem zatwierdzania zarządzania zmianami technicznymi i tworzenie odpowiedniej dokumentacji.

-   Modyfikowanie modelu operacyjnego i wytycznych operacyjnych.

-   Wycofywanie z eksploatacji i usuwanie środowisk źródłowych oraz usług używanych wcześniej przez klienta.

-   Konstruowanie i obsługa środowiska testowego.

-   Instalowanie dodatków Service Pack i innych wymaganych aktualizacji na serwerach infrastruktury.

-   Zapewnianie i konfigurowanie wszelkich publicznych certyfikatów SSL.

-   Redagowanie warunków użytkowania Twojej organizacji do skonfigurowania i wyświetlania na urządzeniach należących do użytkowników końcowych.

### Faza inicjowania

-   Współpraca z zespołem firmy Microsoft, aby rozpocząć dołączanie kwalifikujących się usług.

-   Udział w spotkaniu wstępnym, zarządzanie uczestnikami z Twojej organizacji i przewodzenie im oraz potwierdzanie osi czasu korygowania.

### Faza oceny

-   Wskazanie odpowiednich osób biorących udział w projekcie (w tym kierownika) na potrzeby zrealizowania niezbędnych działań oceny.

-   Jeśli wybierzesz taką opcję, udostępnianie ekranu firmie Microsoft w celu uzyskania wskazówek podczas uruchamiania narzędzi oceniających Twoje środowisko lub subskrypcję usługi Azure RMS.

-   Uczestniczenie w spotkaniach w celu utworzenia listy korekt i przygotowania ogólnego planu dotyczącego między innymi infrastruktury, sieci, administracji, przygotowania synchronizacji katalogów, zabezpieczeń sieci i tożsamości federacyjnych.

-   Uczestniczenie w spotkaniach w celu ustalenia sposobu inicjowania obsługi użytkowników.

-   Uczestniczenie w spotkaniach w celu zaplanowania konfiguracji usług online.

-   Tworzenie planu pomocy technicznej w celu zapewnienia gotowości na migrację.

### Faza korygowania

-   Wykonywanie czynności wymaganych do ukończenia działań korygowania zidentyfikowanych w fazie oceny.

-   Uczestniczenie w spotkaniach kontrolnych.

### Faza włączania

-   Jeśli wybierzesz taką opcję, udostępnianie ekranu firmie Microsoft w celu uzyskania wskazówek podczas wprowadzania zmian w Twoim środowisku lub subskrypcji usługi Azure RMS.

-   Odpowiednie zarządzanie zasobami.

-   Konfigurowanie elementów związanych z siecią zgodnie ze wskazówkami firmy Microsoft.

-   Przygotowywanie katalogów i konfigurowanie synchronizacji katalogów zgodnie ze wskazówkami firmy Microsoft.

-   Konfigurowanie infrastruktury związanej z zabezpieczeniami (na przykład portów zapory) zgodnie ze wskazówkami firmy Microsoft.

-   Wdrażanie odpowiedniej infrastruktury klienckiej.

-   Wdrażanie rozwiązania inicjowania obsługi użytkowników zgodnie ze wskazówkami firmy Microsoft.

-   Włączanie różnych usług zgodnie ze wskazówkami firmy Microsoft.

## Chcesz dowiedzieć się więcej?
Zobacz [Microsoft Azure Rights Management](http://products.office.com/business/microsoft-azure-rights-management) i [Enterprise Mobility Suite](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/default.aspx).

