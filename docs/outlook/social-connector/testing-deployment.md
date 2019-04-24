---
title: 展開のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーのインストールとアンインストールに関してテストする必要があるいくつかのシナリオについて説明します。
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329163"
---
# <a name="testing-deployment"></a>展開のテスト

このトピックでは、Outlook Social Connector (.osc) プロバイダーのインストールとアンインストールに関してテストする必要があるいくつかのシナリオについて説明します。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Outlook のプレゼンスとクライアントコンピューター上の .osc

.osc プロバイダーのインストールに影響を与える要因には、オペレーティングシステムのビット数、outlook のプレゼンスとビット数、outlook で有効になっている .osc などが含まれます。
  
.osc プロバイダーは、.osc の32ビットバージョンまたは64ビットバージョンのどちらかに記述できます。 outlook 2010 と outlook 2013 は、32ビットと64ビットの両方のバージョンで使用できます。 office outlook 2003 と office outlook の2007は、32ビットバージョンでのみ使用できます。 64ビット版の Windows オペレーティングシステムでは、32ビットまたは64ビットのどちらかの Outlook をインストールできます。 32ビットのオペレーティングシステムでは、64ビットではなく32ビットの Outlook をインストールできます。 インストールされている Outlook のバージョンと .osc プロバイダー自体のビット数に応じて、ユーザーは適切なインストーラーを使用して適切なビット数の .osc プロバイダーをインストールする必要があります。 たとえば、64ビット Outlook がインストールされており、.osc プロバイダーがネイティブ COM コンポーネントである場合、32ビットの .osc プロバイダーは機能せず、ユーザーは適切なインストーラーを使用して、64ビットの .osc プロバイダーをインストールする必要があります。
  
.osc プロバイダーの展開コードでは、ユーザーがコンピューター上でサポートされているバージョンの Outlook を使用していることを前提とすることができます。 ただし、現在のバージョンの .osc がクライアントコンピューター上にない場合は、展開コードで、に特別にhttps://g.live.com構築された g リンク url を使用して、適切なバージョンの .osc をダウンロードしてインストールすることができます。 これらの g リンクは、Outlook のバージョンとビット数、およびクライアントコンピューターのロケールによって異なります。 g リンクを使用して、.osc をインストールまたは更新する方法の詳細については、「[インストールチェックリスト](installation-checklist.md)」を参照してください。
  
.osc プロバイダーをインストールする前に、outlook ユーザーは、outlook で .osc アドインが有効になっていることを確認する必要があります。
  
.osc プロバイダーを展開する方法として推奨されるのは、Windows インストーラー (.msi) パッケージを使用する方法です。 次の各シナリオをテストして、プロバイダーの展開が適切に動作することを確認します。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|outlook が存在しません-outlook 2003 または outlook 2007 がインストールされておらず、outlook 2010 または Microsoft outlook 2013 がインストールされておらず、クイック実行で配信されていません。  <br/> |展開は失敗します。  <br/> |
|outlook 2003 または outlook 2007 がインストールされていませんが、outlook 2010 または Microsoft outlook 2013 はクイック実行で配信されています。  <br/> |32ビットプロバイダーが展開されます。  <br/> |
|outlook 2003 または outlook 2007 がインストールされていますが、.osc がインストールされていません。  <br/> |インストーラーによって、.osc とすべてのパッチがインストールされます。 .osc が正常にインストールされると、インストーラーによってプロバイダーが展開されます。  <br/> |
|outlook 2003 または outlook 2007 がインストールされており、以前のバージョンの .osc がインストールされている。  <br/> |インストーラーは、プログラムに g リンクを使用して、.osc を更新し、プロバイダーを展開します。  <br/> |
|Outlook 2003 または2007がインストールされており、.osc は最新の状態です。  <br/> |インストーラーは、32ビットプロバイダーを展開します。  <br/> |
|outlook 2010 または Microsoft outlook 2013 がインストールされていますが、.osc がインストールされていません。  <br/> |インストーラーが失敗し、適切なエラーメッセージが表示されます。  <br/> |
|outlook 2010 または Microsoft outlook 2013 がインストールされており、古いバージョンの .osc がインストールされています。  <br/> |インストーラーは、インストールされている Outlook 2010 または Microsoft outlook 2013 のビット数に適しています。パッチに対する g リンクを介して .osc を更新し、適切なプロバイダーを展開します。  <br/> |
|outlook 2010 または Microsoft outlook 2013 がインストールされており、.osc が最新の状態になっています。  <br/> |インストールされている Outlook 2010 または Microsoft outlook 2013 (32 ビットまたは64ビット) のビット数に適したインストーラーは、適切なプロバイダーを展開します。  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>インストールされている場所とレジストリキー

.osc プロバイダーが展開されているファイルの場所と、プロバイダーのレジストリキーが作成される Windows レジストリ内の場所を確認します。
  
### <a name="file-location-for-osc-provider-dlls"></a>.osc プロバイダ dll のファイルの場所

次の表に示すシナリオをテストします。 表には、.osc プロバイダ dll の既定のインストールパスが一覧表示されている点に注意してください。 ユーザーは、これらの dll をインストールする場所をカスタマイズできます。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|Microsoft Outlook 2013 は、クライアントコンピューターにインストールされます。  <br/> |プロバイダー dll は Office15 フォルダーに展開されます。 オペレーティングシステムが64ビットで、Microsoft Outlook 2013 が32ビットの場合、32ビット dll は C:\Program files (x86) \Microsoft Office\Office15. の下に展開されます。 オペレーティングシステムが64ビットで、Microsoft Outlook 2013 が64ビットの場合、64ビット dll は C:\Program C:\Program Office\Office15. の下に展開されます。 オペレーティングシステムが32ビットの場合、dll は C:\Program C:\Program Office\Office15. の下に展開されます。  <br/> |
|Outlook 2010 は、クライアントコンピューターにインストールされます。  <br/> |プロバイダー dll は Office14 フォルダーに展開されます。 オペレーティングシステムが64ビットで、Outlook 2010 が32ビットの場合、32ビット dll は C:\Program files (x86) \Microsoft Office\Office14. の下に展開されます。 オペレーティングシステムが64ビットで、Outlook 2010 が64ビットの場合、64ビット dll は C:\Program C:\Program Office\Office14. の下に展開されます。 オペレーティングシステムが32ビットの場合、dll は C:\Program C:\Program Office\Office14. の下に展開されます。  <br/> |
|Outlook 2007 は、クライアントコンピューターにインストールされます。  <br/> |プロバイダー dll は C:\Program C:\Program Office\Office14. の下に展開されます。 .osc をインストールすると、Office14 フォルダーが作成され、すべてのプロバイダー dll の前に、.osc をインストールする必要があります。 前のセクション「 [Outlook のプレゼンスと、クライアントコンピューターの .osc](#olosc_TestingDeployment_PresenceOfOutlook)」を参照してください。  <br/> |
|Outlook 2003 は、クライアントコンピューターにインストールされます。  <br/> |プロバイダー dll は C:\Program C:\Program Office\Office14. の下に展開されます。 .osc をインストールすると、Office14 フォルダーが作成され、すべてのプロバイダー dll の前に、.osc をインストールする必要があります。 前のセクション「 [Outlook のプレゼンスと、クライアントコンピューターの .osc](#olosc_TestingDeployment_PresenceOfOutlook)」を参照してください。  <br/> |
|Microsoft Outlook 2013 はインストールされていませんが、クイック実行でクライアントコンピューターに配信されます。  <br/> |プロバイダー dll は Office15 フォルダーに展開されます。 オペレーティングシステムが64ビットの場合、32ビットの dll は c:\program files (x86) \Microsoft Office\Office15 または c:\program c:\program Office\Office15. の下に展開されます。 オペレーティングシステムが32ビットの場合、dll は C:\Program C:\Program Office\Office15. の下に展開されます。 Office15 フォルダーが存在しない場合は、インストールによってフォルダーが作成されます。  <br/> |
|Outlook 2010 はインストールされていませんが、クイック実行でクライアントコンピューターに配信されます。  <br/> |プロバイダー dll は Office14 フォルダーに展開されます。 オペレーティングシステムが64ビットの場合、32ビットの dll は c:\program files (x86) \Microsoft Office\Office14 または c:\program c:\program Office\Office14. の下に展開されます。 オペレーティングシステムが32ビットの場合、dll は C:\Program C:\Program Office\Office14. の下に展開されます。 Office14 フォルダーが存在しない場合は、インストールによってフォルダーが作成されます。  <br/> |
   
### <a name="windows-registry-locations"></a>Windows レジストリの場所

次のことを確認します。
  
- .osc プロバイダインストーラーは、または`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`のいずれかで、Windows レジストリに、.osc プロバイダーの ProgID 値を作成します。 
    
- 例外は、クライアントコンピューターに32ビットの Outlook が64ビットの Windows オペレーティングシステムで実行されている場合です。 この例では、または`HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`のいずれかで ProgID が作成されます。
    
- dll が regsvr32 によって登録されている場合は、そのレジストリキーが同じ場所にある必要があります。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>インストールの削除

次に、アンインストールプロセスが、.osc プロバイダーで正しく動作することを確認するためのいくつかのテストを示します。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|ユーザーがプロバイダーをアンインストールすることを選択します。  <br/> |プロバイダーは dll をアンインストールし、レジストリをクリアします。  <br/> |
|ユーザーがプロバイダーのアンインストールプロセスを取り消すことを選択します。  <br/> |プロバイダーはアンインストールプロセスをキャンセルし、ユーザーをアンインストールプロセスが開始される前の状態に戻します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーの登録](registering-a-provider.md)  
- [インストールチェックリスト](installation-checklist.md)
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)

