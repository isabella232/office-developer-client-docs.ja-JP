---
title: インストール チェックリスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーを正常にインストールするための前提条件と、プロバイダー インストーラーが正常に動作するために完了する必要があるインストール チェックについて説明します。
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286342"
---
# <a name="installation-checklist"></a>インストール チェックリスト

このトピックでは、Outlook Social Connector (OSC) プロバイダーを正常にインストールするための前提条件と、プロバイダー インストーラーが正常に動作するために完了する必要があるインストール チェックについて説明します。
  
## <a name="installation-overview"></a>インストールの概要

ユーザーは、サポート されているバージョンの OSC プロバイダーが存在し、Outlook コンピューターに OSC がインストールされ、有効になっている場合にのみ、OSC プロバイダーをインストールする必要があります。 Outlook のサポート バージョンは、Office Outlook 2003、Office Outlook 2007、Outlook 2010、Outlook 2013 です (クライアント コンピューターにインストールされている場合、または Outlook 2010 および Outlook 2013 の場合は、クライアント コンピューターで クイック実行 によって配信されます)。 インストールが正常に完了するには、プロバイダー インストーラーで次の操作を行う必要があります。
  
- サポートされているバージョンのファイルが存在Outlook確認します。
    
- OSC がインストールされているかどうかを確認します。
    
> [!NOTE]
> クイック実行は、Outlook 2010 (32 ビット) または Outlook 2013 (32 ビット) を実行できる仮想環境です。 2013 Outlook、VirtualOutlook キーがレジストリのHKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook存在Windowsします。 クライアント コンピューターで クイック実行 製品として Outlook を配信する方法の詳細については[、「how to Verify if Outlook](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)is Available on a computer as a クイック実行 Product」を参照してください。 
  
ただし、ユーザーは、プロバイダーをインストールする前に OSC が有効になっている必要があります。
  
OSC プロバイダーを含むサード パーティは、OSC を再配布できません。 ただし、OSC がインストールされていない場合、プロバイダー インストーラーは適切な g-links を使用して OSC をクライアント コンピューターにインストールできます。 g-link は、ユーザーを対応する Web ページに転送して OSC をダウンロードする特別に構築された https://g.live.com URL です。 OSC g-link は https://g.live.com/0CR _LCID_ /  _Glink_ として書式設定され _、LCID_ と _Glink_ はクライアント コンピューター上の Outlookのロケール、バージョン、およびビット数を指定します。 各 g-link は実行可能ファイルをポイントし、指定された  _LCID_ 値と  _Glink 値に固有_ です。 
  
たとえば、LCID 1033 (米国英語) の Outlook 2003 または Outlook 2007 の OSC の最新バージョンをインストールする g リンクは次のとおりです。
  
https://g.live.com/0CR1033/80
  
Outlook の異なるバージョンとビット数の Glink 値、およびサポートされている地域の _LCID_ 値の詳細については、以下の「インストール チェックリスト」の「#7」を [参照](#olosc_InstallationOverview_InstallationChecklist)してください。 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>インストール チェックリスト

プロバイダーセットアップ パッケージは、プロバイダーが正常にインストールされたことを確認するために、図 1 に示すように、一連のインストール チェックを実行する必要があります。
  
**図 1.プロバイダーのインストール ロジック**

![インストール チェックリスト](media/odc_ol14_ta_OSC_Fig07.gif)
  
次の手順では、図 1 に示すインストール チェックについて説明します。
  
1. 前提条件として、インストールまたはOutlookを検出し、インストールされている場合または存在する場合は、OSC のバージョンがサポートOutlook判断します。 インストールされているバージョンの検出方法の詳細については、「Outlookバージョンを確認する」を[参照](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)Outlook。
    
   - インストール済みバージョンのOutlook 2003 より前Outlookプロバイダーのインストール手順を完了できません。 OSC プロバイダーのインストールに進む前に、サポートされているバージョンOutlook OSC を入手してください。
    
   - インストールOutlook場合は、手順 2 に進みます。
    
   - 2003 Outlook 2007 Outlookインストールされている場合は、手順 3 に進みます。 
    
   - 2010 Outlookまたは 2013 Outlookインストールされている場合は、手順 4 に進みます。
    
2. **クライアント コンピューターにインストールされていない場合Outlook手順を実行します。**
    
   1. OSC が 2010 または 2013 の クイック実行 インストールの既定のOutlookインストールOutlookします。 レジストリ内 `VirtualOutlook` の次の場所にあるキー Windowsします。 
      
      - 2010 Outlookの場合、`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - ソーシャル Outlook 2013 の場合、`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      キー  `VirtualOutlook` は、REG_SZのロケール タグ ("en-us" など) を含む値です。 
      
   2. キーが存在しない場合Outlookクライアント コンピューターに存在しない場合、プロバイダーのインストール手順 `VirtualOutlook` を完了できません。 OSC プロバイダーのインストールに進む前に、サポートされているバージョンOutlook OSC を入手してください。 
      
   3. キーが `VirtualOutlook` 存在する場合は、Outlookコンピュータークイック実行によって配信されました。 OSC タイプ ライブラリのインストール済みバージョンを確認するには、次の場所にあるキーをレジストリWindows `OSCVersion` します。 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      値は、タイプ ライブラリのバージョン番号  `OSCVersion` Socialprovider.dll ("1.0"、"1.1"、または "15" など) を指定する文字列です。 
      
   4. `OSCVersion`"1.0"、"1.1" または "15" の場合は、適切なバージョンの OSC がインストールされます。 手順 6 に進み、最新バージョンの OSC Outlookを準備するために、現在のユーザー インターフェイス ロケールを確認します。 
      
   5. それ以外の場合  `OSCVersion` 、予期される値は含めされません。 手順 6 に進み、適切なバージョンの OSC をインストールOutlookする現在のユーザー インターフェイス ロケールを確認します。 
    
3. **クライアント コンピューターに 2003 Outlook 2007 Outlookインストールされている場合は、次の手順に進みます。**
    
   1. 次の修飾されたコンポーネント ID が存在するかどうかをテストするインストーラー カスタム アクションを記述して、OSC がインストールされているかどうかを確認します。
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      修飾されたコンポーネント ID は、ポインターと同様に、単一レベルの間接参照のメソッドを提供する GUID です。 インストーラーの詳細については、「Windowsドキュメント[へのロードマップ」をWindowsしてください](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)。
      
   2. 指定した修飾コンポーネントが存在する場合は、OSC のバージョンがインストールされます。 手順 5 に進み、最新バージョンの OSC Outlook準備するために、現在のユーザー インターフェイス ロケールを確認します。
      
   3. それ以外の場合、OSC はインストールされません。 手順 6 に進み、適切なバージョンの OSC をインストールOutlookする現在のユーザー インターフェイス ロケールを確認します。
      
4. **クライアント コンピューターに 2010 Outlook 2013 Outlookインストールされている場合は、次の手順に進みます。**
    
   1. レジストリ内の次の場所にあるキーを調Outlookして、インストールされているバージョンのコンピューターのビット `Bitness` Windowsします。 
      
      - 2010 Outlookについては、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - 2013 Outlookについては、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      キーは、32 ビット Outlookの場合は `Bitness` "x86"、64 ビット の場合は "x64" Outlook。 
      
   2. プロバイダーが管理プロバイダーであり、ターゲット プラットフォームを **Any CPU** として指定するプロバイダー コンポーネントをコンパイルした場合は、手順 6 に進み、最新バージョンの OSC のインストールを準備するために現在の Outlook ユーザー インターフェイス ロケールを検索します。 プロバイダーは、OSC の 32 ビット バージョンと 64 ビット バージョンの両方で動作します。
      
   3. プロバイダーがネイティブ COM コンポーネントの場合は、インストールされているバージョンのデバイスのビット数をOutlook。
      
      - インストールされているバージョンの Outlook が 32 ビットの場合、適切な OSC がインストールされていることを確認した後、インストール手順で 32 ビット プロバイダーをインストールする必要があります (手順 8)。
      
      - それ以外の場合、インストールされているバージョンの Outlook は 64 ビットであり、適切な OSC がインストールされていることを確認した後、インストール手順で 64 ビット プロバイダーをインストールする必要があります (手順 8)。 
      
   4. 手順 6 に進み、適切なバージョンの OSC Outlookを準備するために、現在のユーザー インターフェイス ロケールを確認します。
    
5. **2003 または Outlook 2007** Outlook OSC がクライアント コンピューターにインストールされている場合は、次の手順に進みます。ユーザー インターフェイスの現在Outlookロケールを確認するには、次の場所にあるキーをレジストリ `OSCLcid` Windowsします。 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   キーは、現在の Outlook ユーザー インターフェイス ロケールを表すインターネット エンジニアリング タスク フォース (IETF) ロケール タグ `OSCLcid` [([RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義) を指定する DWORD 値です。 手順 7 に進み、最新の OSC をクライアント コンピューターにインストールします。
    
6. **Outlook 2003 または Outlook 2007 がインストールされている場合、または Outlook 2010 または Outlook 2013 が存在するが、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、この手順を実行します。**
    
   **LanguageSettings オブジェクトを使用** して、ユーザー インターフェイス ロケールの LCID Outlook決定します。 次のVisual Basicスクリプト エディション (VBScript) コード スニペットは、ユーザー インターフェイス ロケールの LCID を取得Outlook示しています。 
    
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

7. **インストーラーにインストールされているバージョンの LCID Outlook があるが、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、次の手順を実行します。**
    
   g-link をインストール パッケージにチェーンして、最新バージョンの OSC がクライアント コンピューターにインストールされていることを確認します。 g-link 形式は次のとおりです。
    
   https://g.live.com/0CR_LCID_ / _Glink_
    
   サポートされている LCID 値については、以下の表 1、サポートされている  _Glink_ 値については表 2  _を参照_ してください。 たとえば、32 ビット Outlook Social Connector 2013 (米国英語) 用の 32 ビット OSC の最新バージョンをインストールする g-link は次のとおりです。 
    
   https://g.live.com/0CR1033/82
    
8. プロバイダーをインストールします。 プロバイダーのインストール手順では、プログラム識別子 (ProgID) をレジストリの適切な場所Windowsする必要があります。 詳細については、「プロバイダーの [登録」を参照してください](registering-a-provider.md)。 また、インストールするプロバイダーのビット数が、クライアント コンピューターに存在するバージョンのビットOutlook同じことを確認してください。 たとえば、32 ビット Outlook 2013 が存在する場合は 32 ビット プロバイダーをインストールし、64 ビット Outlook 2013 がインストールされている場合は 64 ビット プロバイダーをインストールします。 2003 Outlook 2007 の場合、プロバイダーの 32 ビット バージョンだけが適用されます。 
    
**表 1: OSC でサポートされているロケールと対応する LCID 値 (16 進数)**
  
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
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**表 2: OSC でサポートされている Glink 値**
  
|**Glink 値**|**Function**|
|:-----|:-----|
|80  <br/> |最新バージョンの OSC for Outlook 2003 または Outlook 2007 をインストールします。  <br/> |
|82  <br/> |Outlook 2007、Outlook 2010、または Outlook Social Connector 2013 用の 32 ビット OSC の最新パッチをインストールします。  <br/> |
|83  <br/> |Outlook 2010 または Outlook Social Connector 2013 用の 64 ビット OSC の最新パッチをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーの登録](registering-a-provider.md) 
- [プロバイダーを開発するための学習のクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーの展開](deploying-a-provider.md)

