---
title: インストール チェックリスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーを正常にインストールするための前提条件について説明します。また、プロバイダーのインストーラーが正常に動作することを確認する必要があります。
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286342"
---
# <a name="installation-checklist"></a>インストール チェックリスト

このトピックでは、Outlook Social Connector (.osc) プロバイダーを正常にインストールするための前提条件について説明します。また、プロバイダーのインストーラーが正常に動作することを確認する必要があります。
  
## <a name="installation-overview"></a>インストールの概要

ユーザーは、Outlook のサポートバージョンが存在し、.osc がインストールされてクライアントコンピューターに有効になっている場合にのみ、.osc プロバイダーをインストールする必要があります。 outlook のバージョンをサポートしているのは、office outlook 2003、office outlook 2007、outlook 2010、outlook 2013 (クライアントコンピューターにインストールされているか、outlook 2010 および outlook の場合は、クライアントコンピューター上でクイック実行が配信される場合) です。 インストールが正常に行われるように、プロバイダーのインストーラーは次の操作を実行する必要があります。
  
- サポートされているバージョンの Outlook があるかどうかを確認します。
    
- .osc がインストールされているかどうかを確認します。
    
> [!NOTE]
> クイック実行は、outlook 2010 (32 ビット) または outlook 2013 (32 ビット) が実行できる仮想環境です。 Outlook 2013 の場合は、Windows レジストリの HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook に virtualoutlook キーが存在するかどうかを確認します。 クイック実行製品として outlook をクライアントコンピューターに配信する方法の詳細については、「[クイック実行製品としてコンピューター上で outlook が利用可能かどうかを確認する方法](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)」を参照してください。 
  
ただし、ユーザーは、プロバイダーをインストールする前に、.osc が有効になっていることを確認する必要があります。
  
.osc プロバイダーを含むサードパーティは、.osc を再配布できません。 ただし、.osc がインストールされていない場合、プロバイダーインストーラーは適切な g リンクを使用して、クライアントコンピューターに .osc をインストールすることができます。 g リンクは、ユーザーを対応する web ページhttps://g.live.comに転送して、.osc をダウンロードするための特別に構築された URL です。 .osc g リンクは、 https://g.live.com/0CR _lcid_/ _glink_として書式設定されます。 _lcid_と_glink_では、クライアントコンピューター上の Outlook のロケール、バージョン、ビットが指定されます。 各 g リンクは、実行可能ファイルを指しており、指定された_LCID_および_glink_値に固有のものです。 
  
たとえば、LCID 1033 (米国英語) 用の outlook 2003 または outlook 2007 用の最新バージョンの .osc をインストールするための g リンクは次のようになります。
  
https://g.live.com/0CR1033/80
  
Outlook のさまざまなバージョンとビットの_リンク_値、およびサポートされるロケールの_LCID_値の詳細については、次のセクション「[インストールチェックリスト](#olosc_InstallationOverview_InstallationChecklist)」の「#7」を参照してください。 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>インストール チェックリスト

プロバイダーのセットアップパッケージは、図1に示すように、一連のインストールチェックを実行して、プロバイダーが正常にインストールされるようにする必要があります。
  
**図1。プロバイダーのインストールロジック**

![インストール チェックリスト](media/odc_ol14_ta_OSC_Fig07.gif)
  
次の手順では、図1に示されているインストールの確認について説明します。
  
1. 前提条件として、outlook がインストールされているかどうかを検出し、インストールされているか存在している場合は、outlook のバージョンが .osc をサポートしているかどうかを判断します。 インストールされている outlook のバージョンを検出する方法については、「 [outlook のバージョンを確認](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)する」を参照してください。
    
   - インストールされている outlook のバージョンが outlook 2003 より前の場合は、プロバイダーのインストール手順を完了できません。 ユーザーに、サポートされているバージョンの Outlook と .osc を入手してから、.osc プロバイダーをインストールするように通知します。
    
   - Outlook がインストールされていない場合は、手順2に進みます。
    
   - outlook 2003 または outlook 2007 がインストールされている場合は、手順3に進みます。 
    
   - outlook 2010 または outlook 2013 がインストールされている場合は、手順4に進みます。
    
2. **クライアントコンピューターに Outlook がインストールされていない場合は、次の手順を続行します。**
    
   1. outlook 2010 または outlook 2013 のクイック実行インストールの既定のコンポーネントとして、.osc がインストールされているかどうかを確認します。 Windows レジストリ`VirtualOutlook`の次の場所にあるキーを調べます。 
      
      - Outlook 2010 の場合`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Outlook Social Connector 2013 の場合`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      `VirtualOutlook`キーは、インストールされている製品の "en-us" などのロケールタグを含む REG_SZ 値です。 
      
   2. この`VirtualOutlook`キーが存在しない場合、Outlook はクライアントコンピューターに存在せず、プロバイダーのインストール手順を完了できません。 ユーザーに、サポートされているバージョンの Outlook と .osc を入手してから、.osc プロバイダーをインストールするように通知します。 
      
   3. このキー `VirtualOutlook`が存在する場合、Outlook はクイック実行でクライアントコンピューターに配信されていました。 Windows レジストリの次の場所にある`OSCVersion`キーを調べて、インストールされている .osc タイプライブラリのバージョンを確認します。 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      の`OSCVersion`値は、形式ライブラリのバージョン番号を指定する文字列です (たとえば、"1.0"、"1.1"、または "15")。 
      
   4. が`OSCVersion` "1.0"、"1.1"、または "15" の場合は、適切なバージョンの .osc がインストールされています。 手順6に進み、最新バージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。 
      
   5. それ以外`OSCVersion`の場合は、予期される値を含みません。 手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。 
    
3. **outlook 2003 または outlook 2007 がクライアントコンピューターにインストールされている場合は、次の手順を続行します。**
    
   1. 次の修飾されたコンポーネント ID が存在するかどうかをテストするインストーラーカスタムアクションを記述して、.osc がインストールされているかどうかを確認します。
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      修飾コンポーネント ID は、ポインターに似た単一レベルの間接的なメソッドを提供する GUID です。 windows インストーラーの詳細については、「 [windows インストーラーのドキュメントのロードマップ](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)」を参照してください。
      
   2. 指定した修飾コンポーネントが存在する場合は、.osc のバージョンがインストールされます。 手順5に進み、最新バージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。
      
   3. それ以外の場合は、.osc がインストールされません。 手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。
      
4. **outlook 2010 または outlook 2013 がクライアントコンピューターにインストールされている場合は、次の手順を続行します。**
    
   1. Windows レジストリの以下の場所にある`Bitness`キーを調べて、インストールされている Outlook のバージョンのビット数を確認します。 
      
      - Outlook 2010 の場合は、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Outlook 2013 の場合は、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      キー `Bitness`は、32ビット outlook の場合は "x86"、64ビットの outlook の場合は "x64" です。 
      
   2. プロバイダーがマネージドプロバイダーで、ターゲットプラットフォームを指定したプロバイダコンポーネントを**任意の CPU**としてコンパイルした場合は、手順6に進み、最新バージョンの .osc のインストールを準備するための現在の Outlook ユーザーインターフェイスロケールを見つけます。 プロバイダーは、この .osc の32ビットバージョンと64ビットバージョンの両方で機能します。
      
   3. プロバイダーがネイティブ COM コンポーネントの場合は、インストールされている Outlook のバージョンのビット数を確認します。
      
      - インストールされている Outlook のバージョンが32ビットである場合は、適切な .osc がインストールされていることを確認した後に、インストール手順で32ビットのプロバイダー (手順 8) をインストールする必要があります。
      
      - インストールされている Outlook のバージョンが64ビットである場合は、適切な .osc がインストールされていることを確認した後、インストール手順で64ビットのプロバイダー (手順 8) をインストールする必要があります。 
      
   4. 手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。
    
5. **outlook 2003 または outlook 2007 がインストールされており、クライアントコンピューターに .osc がインストールされている場合は、この手順を続行します。** Windows レジストリの次の場所にある`OSCLcid`キーを調べて、現在の Outlook ユーザーインターフェイスのロケールを確認します。 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   `OSCLcid`キーは、現在の Outlook ユーザーインターフェイスのロケールを表す、インターネット技術標準化委員会 (IETF) のロケールタグ ( [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)および[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義) を指定する DWORD 値です。 手順7に進み、クライアントコンピューターに最新の .osc をインストールします。
    
6. **outlook 2003 または outlook 2007 がインストールされているか、outlook 2010 または outlook 2013 がインストールされている場合に、この手順を続行します。ただし、最新の .osc が必ずしもクライアントコンピューターにインストールされるとは限りません。**
    
   **言語設定**オブジェクトを使用して、Outlook ユーザーインターフェイスのロケールの LCID を特定します。 次の Visual Basic Scripting Edition (VBScript) コードスニペットは、Outlook ユーザーインターフェイスロケールの LCID を取得する方法を示しています。 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **インストーラーにインストールされているバージョンの Outlook の LCID がある場合は、次の手順に進みます。最新の .osc は、必ずしもクライアントコンピューターにインストールされません。**
    
   インストールパッケージに g リンクをチェーンして、最新バージョンの .osc がクライアントコンピューターにインストールされていることを確認します。 g リンクの形式は次のとおりです。
    
   https://g.live.com/0CR_LCID_/  _glink_
    
   サポートされている_LCID_値については、表1を参照してください。サポートされている_glink_値については、表2を参照してください。 たとえば、次のように、32ビットの Outlook Social Connector 2013 (米国英語) 用に32ビットの .osc の最新バージョンをインストールするための g リンクがあります。 
    
   https://g.live.com/0CR1033/82
    
8. プロバイダーをインストールします。 プロバイダーのインストール手順では、プログラム id (ProgID) を適切な Windows レジストリの場所に登録する必要があります。 詳細については、「[プロバイダーの登録](registering-a-provider.md)」を参照してください。 また、インストールするプロバイダーのビット数が、クライアントコンピューター上に存在する Outlook のバージョンのビットと同じであることを確認してください。 たとえば、32ビットの outlook 2013 が存在する場合は、32ビットのプロバイダーをインストールし、64ビットの outlook をインストールしている場合は、64ビットのプロバイダーをインストールします。 Outlook 2003 または2007の場合は、使用しているプロバイダーの32ビットバージョンのみが適用されます。 
    
**表 1: サポートされているロケールおよび対応する LCID 値を、.osc の16進数で指定します。**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|ja-jp  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kk-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|cyrl-cs  <br/> |3098  <br/> |
|latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**表 2: .osc のサポートされている glink 値**
  
|**glink 値**|**Function**|
|:-----|:-----|
|80  <br/> |outlook 2003 または outlook 2007 用の最新バージョンの .osc をインストールします。  <br/> |
|82  <br/> |outlook 2007、outlook 2010、または outlook Social Connector 2013 用に32ビットの詳細な更新プログラムをインストールします。  <br/> |
|83  <br/> |outlook 2010 または outlook Social Connector 2013 用に64ビットの詳細な更新プログラムをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーの登録](registering-a-provider.md) 
- [プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開する](deploying-a-provider.md)

