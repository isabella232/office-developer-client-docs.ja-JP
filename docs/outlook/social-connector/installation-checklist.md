---
title: インストール チェックリスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Outlook ソーシャル コネクタ (OSC) プロバイダーを正常にインストールするための前提条件について説明し、インストールが正常に動作する、プロバイダーのインストーラーを完了しなければならないことを確認します。
ms.openlocfilehash: cb8ed24db28c3b0e945c4db4b2daa4a2470d7dd5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804349"
---
# <a name="installation-checklist"></a>インストール チェックリスト

Outlook ソーシャル コネクタ (OSC) プロバイダーを正常にインストールするための前提条件について説明し、インストールが正常に動作する、プロバイダーのインストーラーを完了しなければならないことを確認します。
  
## <a name="installation-overview"></a>インストールの概要

ユーザーは、サポートのバージョンの Outlook が存在し、OSC がインストールされ、クライアント コンピューターで有効になっている場合にのみ、OSC プロバイダーをインストールする必要があります。 サポートのバージョンの Outlook は、Office Outlook 2003、Office Outlook 2007、Outlook 2010、Outlook 2013 の (またはをインストール クライアント コンピューターで、Outlook 2010、Outlook 2013、クライアント コンピューター上でクイック実行で提供)。 インストールの成功を確実には、プロバイダー インストーラーする必要があります、次の操作。
  
- Outlook のサポートされているバージョンが存在するかどうかを確認します。
    
- OSC がインストールされているかどうかを確認します。
    
> [!NOTE]
> クイック実行は、Outlook 2010 (32 ビット) または Outlook 2013 (32 ビット) を実行できる仮想環境です。 Outlook 2013 では、Windows レジストリの HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook の VirtualOutlook キーが存在するかを確認します。 クライアント コンピューター上のクイック実行製品として Outlook を提供することに関する詳細については、 [Outlook がクイック実行の製品としてのコンピューターで利用可能である場合に確認する方法](http://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)を参照してください。 
  
ユーザーは、ただし、プロバイダーをインストールする前に、OSC が有効になっていることを確認するのにはあります。
  
OSC プロバイダーを含む第三者は、OSC を再配布できません。 ただし、OSC がインストールされていない場合、プロバイダー インストーラーを使用して g の該当するリンク、OSC をクライアント コンピューターにインストールします。 G ・ リンクでは、特別に作成された URL のhttp://g.live.com、OSC をダウンロードするには、対応する web ページにユーザーを転送します。 OSC の g ・ リンクが設定されてhttp://g.live.com/0CR _LCID_/ _Glink_、 _LCID_と_Glink_ 、ロケール、バージョン、およびクライアント コンピューター上 Outlook のビット数を指定します。 各 g リンクは、実行可能ファイルをポイントし、指定された_LCID_と_Glink_の値に固有します。 
  
たとえば、Outlook 2003 の OSC または LCID の 1033 (英語版) の Outlook 2007 の最新バージョンをインストールするのには g ・ リンクはとおりです。
  
http://g.live.com/0CR1033/80
  
_Glink_さまざまなバージョンと、Outlook のビット数の値とサポートされているロケールの_LCID_値についての詳細は、7 の「次の[インストール チェックリスト](#olosc_InstallationOverview_InstallationChecklist)を参照してください。 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>インストール チェックリスト

プロバイダーのセットアップ パッケージは、プロバイダーが正常にインストールされることを確認するのには、図 1 に示すように、一連のインストールのチェックを実行する必要があります。
  
**図 1 です。プロバイダーのインストール ロジック**

![インストール チェックリスト](media/odc_ol14_ta_OSC_Fig07.gif)
  
次の手順では、図 1 に記載されているインストールの確認について説明します。
  
1. 前提条件として Outlook がインストールされているかどうかを検出またはとインストールされている、または存在、Outlook のバージョンが、OSC をサポートしているかどうかを決定します。 インストールされている Outlook のバージョンの検出の詳細については、 [Outlook のバージョンを確認して](http://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)参照してください。
    
   - インストールされているバージョンの Outlook が Outlook 2003 より前の場合は、プロバイダーのインストール手順を完了できません。 OSC プロバイダーをインストールするには、Outlook と作業を進める前に OSC のサポートされているバージョンを入手するのにはユーザーに通知します。
    
   - Outlook がインストールされていない場合は、手順 2 に進みます。
    
   - Outlook 2003 または Outlook 2007 がインストールされている場合は、手順 3 に進みます。 
    
   - Outlook 2010 または Outlook 2013 をインストールする場合は、手順 4 に進みます。
    
2. **クライアント コンピューターに Outlook がインストールされていない場合は、この手順に進みます。**
    
   1. OSC が Outlook 2010 または Outlook 2013 のクイック実行のインストールの既定のコンポーネントとしてインストールされているかどうかを確認してください。 調べて、`VirtualOutlook`キーを Windows レジストリに次の場所にします。 
      
      - Outlook 2010 では、`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Outlook ソーシャル コネクタ 2013 年の`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      `VirtualOutlook`キーは、REG_SZ 値を次のようにロケール タグが含まれています"en-私たち"、インストールされている製品のです。 
      
   2. 場合、`VirtualOutlook`キーが存在しない、Outlook は、クライアント コンピューター上に存在しない、およびプロバイダーのインストール手順を完了できません。 OSC プロバイダーをインストールするには、Outlook と作業を進める前に OSC のサポートされているバージョンを入手するのにはユーザーに通知します。 
      
   3. 場合、`VirtualOutlook`キーが存在して、クライアント コンピューターに Outlook がクイック実行で配信されました。 OSC のタイプ ライブラリのインストールされているバージョンを調べることによってチェックに進んで、`OSCVersion`キーを Windows レジストリに次の場所。 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      値`OSCVersion`Socialprovider.dll (たとえば、「1.0」、「1.1」、または「15」) のタイプ ライブラリのバージョン番号を指定する文字列します。 
      
   4. 場合`OSCVersion`「1.0」、「1.1」、または「15」には、OSC の適切なバージョンがインストールされています。 OSC の最新バージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するのには 6 の手順に進みます。 
      
   5. それ以外の場合、 `OSCVersion` 、予期される値が含まれていません。 OSC の適切なバージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するのには 6 の手順に進みます。 
    
3. **Outlook 2003 または Outlook 2007 がクライアント コンピューターにインストールされている場合は、この手順に進みます。**
    
   1. インストーラーを記述することによって、OSC がインストールされているかどうかを確認して次の制限されたコンポーネントの ID の存在をテストするのにはカスタムの動作。
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      制限されたコンポーネントの ID は、単一レベルの間接指定のポインターのようなメソッドを提供する GUID です。 Windows インストーラーの詳細については、 [Windows インストーラーのドキュメントへのロードマップ](http://msdn.microsoft.com/library/_msi_roadmap_to_windows_installer_documentation.aspx)を参照してください。
      
   2. 修飾された、指定したコンポーネントが存在する場合は、OSC のバージョンがインストールされています。 OSC の最新バージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するのには 5 の手順に進みます。
      
   3. それ以外の場合、OSC はインストールされていません。 OSC の適切なバージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するのには 6 の手順に進みます。
      
4. **Outlook 2010 または Outlook 2013 は、クライアント コンピューターにインストールされている場合は、この手順に進みます。**
    
   1. 調べることによってインストールされているバージョンの Outlook のビット数を決定する、`Bitness`キーを Windows レジストリに次の場所にします。 
      
      - Outlook 2010 では、を確認します。`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Outlook 2013 では、を確認します。`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      `Bitness` 32 ビット Outlook、または 64 ビットの Outlook 用には、「x64」キーは、"x86"です。 
      
   2. プロバイダーは、マネージ プロバイダーでは、ターゲット プラットフォームを指定する**任意の CPU**としてプロバイダー コンポーネントをコンパイルした場合は、手順 6、OSC の最新バージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するに進みます。 プロバイダーは、OSC の 32 ビットと 64 ビットの両方のバージョンで動作します。
      
   3. プロバイダーがネイティブな COM コンポーネントの場合は、インストールされているバージョンの Outlook のビット数を確認してください。
      
      - インストールされている Outlook のバージョンが 32 ビットの場合は、インストール手順は、適切な OSC がインストールされていることを確認した後 (手順 8) で 32 ビットのプロバイダーをインストールする必要があります。
      
      - それ以外の場合、インストールされている Outlook のバージョンは、64 ビットのインストール手順は、適切な OSC がインストールされていることを確認した後 (手順 8) での 64 ビット プロバイダーをインストールする必要があります。 
      
   4. OSC の適切なバージョンをインストールするために準備するのには現在の Outlook ユーザー インターフェイスのロケールを検索するのには 6 の手順に進みます。
    
5. **の OSC は、クライアント コンピューターにインストールされている Outlook 2003 または Outlook 2007 がインストールされている場合に、この手順に進みます:** 調べることによって現在の Outlook ユーザー インターフェイスのロケールを確認して、`OSCLcid`キーを Windows レジストリに次の場所にします。 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   `OSCLcid`キーは、現在の Outlook ユーザー インターフェイスのロケールを表す、インターネット技術標準化委員会 (IETF) のロケール タグ ( [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)で定義されている) を指定する DWORD 値です。 クライアント コンピューターに最新の OSC をインストールするのには 7 の手順に進みます。
    
6. **Outlook 2003 または Outlook 2007 がインストールされているか、または Outlook 2010 または Outlook 2013 ありますが、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、この手順に進みます。**
    
   **LanguageSettings**オブジェクトを使用すると、Outlook のユーザー インターフェイスのロケールの LCID を決定します。 次の Visual Basic スクリプト版 (VBScript) コード スニペットでは、Outlook のユーザー インターフェイスのロケールの LCID を取得する方法を示します。 
    
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

7. **インストーラーがインストールされているバージョンの Outlook での LCID には、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、この手順に進みます。**
    
   インストール パッケージ内に g ・ リンクのチェーン、OSC の最新バージョンがクライアント コンピューターにインストールされていることを確認します。 G リンクの形式は次のとおりです。
    
   http://g.live.com/0CR_LCID_/  _Glink_
    
   サポートされている_LCID_値は、次の表 1 およびサポートされている_Glink_値の表 2 を参照してください。 たとえば、32 ビット Outlook ソーシャル コネクタ 2013 (英語版) の 32 ビットの OSC の最新バージョンをインストールするのには g ・ リンクはとおりです。 
    
   http://g.live.com/0CR1033/82
    
8. プロバイダーをインストールします。 プロバイダーのインストール手順は、Windows レジストリの適切な場所にプログラム id (ProgID) を登録する必要があります。 詳細については、[プロバイダーを登録する](registering-a-provider.md)を参照してください。 また、インストールされているプロバイダーのビット数は、クライアント コンピューター上に存在する Outlook のバージョンのビットと同じことを確認してください。 64 ビットの Outlook 2013 がインストールされている場合、32 ビット Outlook 2013 が存在する場合は、32 ビット プロバイダーと 64 ビット プロバイダーをたとえば、インストールします。 Outlook 2003 または 2007 の場合は、プロバイダーの 32 ビット バージョンのみが適用されます。 
    
**表 1: サポートされているロケールと、OSC の 16 進数に対応する LCID 値**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl es  <br/> |1110  <br/> |
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
|sr-アゼルバイジャン-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**OSC の Glink がサポートされている値を表 2:**
  
|**Glink 値**|**�֐�**|
|:-----|:-----|
|80  <br/> |OSC Outlook 2003 または Outlook 2007 用の最新バージョンをインストールします。  <br/> |
|82  <br/> |Outlook 2007、Outlook 2010 または Outlook ソーシャル コネクタ 2013 の 32 ビットの OSC の最新の修正プログラムをインストールします。  <br/> |
|83  <br/> |Outlook 2010 または Outlook ソーシャル コネクタ 2013 の 64 ビットの OSC の最新の修正プログラムをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーを登録します。](registering-a-provider.md) 
- [プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開します。](deploying-a-provider.md)

