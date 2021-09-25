---
title: 展開のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: このトピックでは、ソーシャル コネクタ (OSC) プロバイダーのインストールとアンインストールについてテストする必要Outlookについて説明します。
ms.openlocfilehash: 3860deb1157477f156b0fae1506c5c6b08699786
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590353"
---
# <a name="testing-deployment"></a>展開のテスト

このトピックでは、ソーシャル コネクタ (OSC) プロバイダーのインストールとアンインストールについてテストする必要Outlookについて説明します。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>クライアント コンピューター Outlook OSC の存在

OSC プロバイダーのインストールに影響を与える要因には、オペレーティング システムのビット数、Outlook の有無とビット数、および Outlook で有効になっている OSC が含まれます。
  
OSC プロバイダーは、32 ビットバージョンまたは 64 ビット バージョンの OSC 用に記述できます。 Outlook 2010 および Outlook 2013 は 32 ビットバージョンと 64 ビット バージョンの両方で使用できます。Office Outlook 2003 および Office Outlook 2007 は 32 ビット バージョンでのみ使用できます。 64 ビット Windowsオペレーティング システムでは、32 ビットまたは 64 ビットのデバイスをインストールOutlook。 32 ビット オペレーティング システムでは、32 ビットのみインストールできますが、64 ビットのオペレーティング システムOutlook。 インストールされているバージョンの Outlook と OSC プロバイダー自体のビット数に応じて、ユーザーは適切なインストーラーを使用して、適切なビット数の OSC プロバイダーをインストールする必要があります。 たとえば、64 ビット Outlook がインストールされ、OSC プロバイダーがネイティブ COM コンポーネントである場合、32 ビット OSC プロバイダーは機能し、ユーザーは適切なインストーラーを使用して 64 ビット OSC プロバイダーをインストールする必要があります。
  
OSC プロバイダーの展開コードは、ユーザーがコンピューター上にサポートされているバージョンのOutlook想定できます。 ただし、現在のバージョンの OSC がクライアント コンピューター上にない場合は、展開コードで特別に構築された g-link URL を使用して、適切なバージョンの OSC をダウンロードしてインストールできます https://g.live.com 。 これらの g-links は、クライアント コンピューターのバージョンとビットOutlookとロケールによって異なります。 g-links を使用して OSC をインストールまたは更新する方法の詳細については、「インストール チェックリスト」 [を参照してください](installation-checklist.md)。
  
OSC プロバイダーをインストールする前Outlookユーザーは、OSC アドインがコンピューターで有効Outlook。
  
OSC プロバイダーを展開する推奨される方法は、Windows (.msi) パッケージを使用します。 次の各シナリオをテストして、展開がプロバイダーに適切に動作するを確認します。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|Outlookが存在しない - Outlook 2003 または Outlook 2007 はインストールされていません。Outlook 2010 または Microsoft Outlook 2013 はインストールされていないか、クイック実行 によって配信されていません。  <br/> |展開は失敗します。  <br/> |
|Outlook 2003 または Outlook 2007 はインストールされていませんが、Outlook 2010 または Microsoft Outlook 2013 は、クイック実行 によって配信クイック実行。  <br/> |32 ビット プロバイダーが展開されます。  <br/> |
|Outlook 2003 または Outlook 2007 がインストールされますが、OSC はインストールされていません。  <br/> |インストーラーは、OSC とすべてのパッチをインストールします。 OSC が正常にインストールされると、インストーラーによってプロバイダーが展開されます。  <br/> |
|Outlook 2003 または Outlook 2007 がインストールされ、以前のバージョンの OSC がインストールされています。  <br/> |インストーラーは、パッチへの g リンクを介して OSC を更新し、プロバイダーを展開します。  <br/> |
|Outlook 2003 または 2007 がインストールされ、OSC が最新です。  <br/> |インストーラーは 32 ビット プロバイダーを展開します。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013インストールされているが、OSC はインストールされていません。  <br/> |インストーラーが失敗し、適切なエラー メッセージが表示されます。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013インストールされ、以前のバージョンの OSC がインストールされています。  <br/> |インストールされている Outlook 2010 または Microsoft Outlook 2013 のビットに適したインストーラーは、g リンクを介してパッチに OSC を更新し、適切なプロバイダーを展開します。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013インストールされ、OSC が最新です。  <br/> |インストールされている Outlook 2010 または Microsoft Outlook 2013 (32 ビットまたは 64 ビット) のビットに適したインストーラーは、適切なプロバイダーを展開します。  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>インストールされている場所とレジストリ キー

OSC プロバイダーが展開されているファイルの場所と、プロバイダーのレジストリ キーが作成される Windows レジストリ内の場所を確認します。
  
### <a name="file-location-for-osc-provider-dlls"></a>OSC プロバイダー DLL のファイルの場所

次の表に示すシナリオをテストします。 表に、OSC プロバイダー DLL の既定のインストール パスを示します。 ユーザーは、これらの DLL をインストールする場所をカスタマイズできます。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|Microsoft Outlook 2013コンピューターにインストールされている場合。  <br/> |プロバイダー DLL は Office15 フォルダーに展開されます。 オペレーティング システムが 64 ビットで Microsoft Outlook 2013 が 32 ビットの場合、32 ビット DLL は C:\Program Files (x86)\Microsoft Office\Office15 の下に展開されます。 オペレーティング システムが 64 ビットで Microsoft Outlook 2013 が 64 ビットの場合、64 ビット DLL は C:\Program Files\Microsoft Office\Office15 の下に展開されます。 オペレーティング システムが 32 ビットの場合、DLL は C:\Program Files\Microsoft Office\Office15 の下に展開されます。  <br/> |
|Outlook 2010 がクライアント コンピューターにインストールされています。  <br/> |プロバイダー DLL は Office14 フォルダーに展開されます。 オペレーティング システムが 64 ビットで、Outlook 2010 が 32 ビットの場合、32 ビット DLL は C:\Program Files (x86)\Microsoft Office\Office14 の下に展開されます。 オペレーティング システムが 64 ビットで、Outlook 2010 が 64 ビットの場合、64 ビット DLL は C:\Program Files\Microsoft Office\Office14 の下に展開されます。 オペレーティング システムが 32 ビットの場合、DLL は C:\Program Files\Microsoft Office\Office14 の下に展開されます。  <br/> |
|Outlook 2007 がクライアント コンピューターにインストールされています。  <br/> |プロバイダー DLL は、C:\Program Files\Microsoft Office\Office14 の下に展開されます。 OSC をインストールすると Office14 フォルダーが作成され、プロバイダー DLL の前に OSC をインストールする必要があります。 前のセクション[「Presence of Outlookクライアント コンピューター上の OSC」を参照してください](#olosc_TestingDeployment_PresenceOfOutlook)。  <br/> |
|Outlook 2003 がクライアント コンピューターにインストールされています。  <br/> |プロバイダー DLL は、C:\Program Files\Microsoft Office\Office14 の下に展開されます。 OSC をインストールすると Office14 フォルダーが作成され、プロバイダー DLL の前に OSC をインストールする必要があります。 前のセクション[「Presence of Outlookクライアント コンピューター上の OSC」を参照してください](#olosc_TestingDeployment_PresenceOfOutlook)。  <br/> |
|Microsoft Outlook 2013はインストールされていませんが、クライアント コンピュータークイック実行によって配信されます。  <br/> |プロバイダー DLL は Office15 フォルダーに展開されます。 オペレーティング システムが 64 ビットの場合、32 ビット DLL は C:\Program Files (x86)\Microsoft Office\Office15 または C:\Program Files\Microsoft Office\Office15 の下に展開されます。 オペレーティング システムが 32 ビットの場合、DLL は C:\Program Files\Microsoft Office\Office15 の下に展開されます。 Office15 フォルダーが存在しない場合、インストールによってフォルダーが作成されます。  <br/> |
|Outlook 2010 はインストールされていませんが、クライアント コンピュータークイック実行によって配信されます。  <br/> |プロバイダー DLL は Office14 フォルダーに展開されます。 オペレーティング システムが 64 ビットの場合、32 ビット DLL は C:\Program Files (x86)\Microsoft Office\Office14 または C:\Program Files\Microsoft Office\Office14 の下に展開されます。 オペレーティング システムが 32 ビットの場合、DLL は C:\Program Files\Microsoft Office\Office14 の下に展開されます。 Office14 フォルダーが存在しない場合、インストールによってフォルダーが作成されます。  <br/> |
   
### <a name="windows-registry-locations"></a>Windowsの場所

次のことを確認します。
  
- OSC プロバイダー インストーラーは、OSC プロバイダーの ProgID 値を、Windowsレジストリに作成 `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` します `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。 
    
- 例外は、クライアント コンピューターに 32 ビット のOutlook 64 ビット オペレーティング システムで実行Windowsです。 この場合、ProgID はどちらかまたはで作成  `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` されます  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。
    
- レジストリ キーは同じで、代わりに DLL がユーザーによって登録されている場合は、同じ場所regsvr32.exe。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>インストールの削除

OSC プロバイダーに対してアンインストール プロセスが正しく動作するを確認するテストを次に示します。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|ユーザーはプロバイダーのアンインストールを選択します。  <br/> |プロバイダーは DLL をアンインストールし、レジストリをクリアします。  <br/> |
|ユーザーは、プロバイダーのアンインストール プロセスを取り消す選択をします。  <br/> |プロバイダーはアンインストール プロセスをキャンセルし、アンインストール プロセスが開始される前にユーザーを状態に戻します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーの登録](registering-a-provider.md)  
- [インストール チェックリスト](installation-checklist.md)
- [OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)

