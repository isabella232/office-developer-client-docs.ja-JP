---
title: 展開のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: このトピックをインストールして、Outlook ソーシャル コネクタ (OSC) プロバイダーをアンインストールに関するテストをするいくつかのシナリオについて説明します。
ms.openlocfilehash: 0494d2ecab446b7da091f80df02267e281987d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804476"
---
# <a name="testing-deployment"></a>展開のテスト

このトピックをインストールして、Outlook ソーシャル コネクタ (OSC) プロバイダーをアンインストールに関するテストをするいくつかのシナリオについて説明します。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Outlook クライアント コンピューターで OSC の存在

要因には、OSC プロバイダーのインストールに影響を与えるには、オペレーティング システム、存在と、Outlook のビット数と Outlook で有効にされている OSC のビットが含まれています。
  
32 ビットまたは 64 ビットのいずれかのバージョンの OSC、OSC プロバイダーを記述できます。 Outlook 2010、Outlook 2013 では、32 ビットと 64 ビットの両方のバージョンで利用できると、Office Outlook 2003 および Office Outlook 2007 では、唯一の 32 ビット バージョンで利用できます。 64 ビット Windows オペレーティング ・ システムでは、32 ビットまたは 64 ビットのいずれかの Outlook をインストールできます。 32 ビット ・ オペレーティング ・ システムをインストールできますのみの 32 ビットが 64 ビットの Outlook です。 によってインストールされているバージョンの Outlook と OSC プロバイダー自体のビット数、ユーザーは、適切なビットの OSC プロバイダーをインストールするのには適切なインストーラーを使用する必要があります。 などの 64 ビットの Outlook がインストールされている場合は、OSC プロバイダーは、ネイティブ COM コンポーネントを 32 ビットの OSC プロバイダーは動作せず、ユーザーは、64 ビットの OSC プロバイダーをインストールするのには適切なインストーラーを使用する必要があります。
  
OSC プロバイダーの展開コードは、ユーザーがコンピューター上の Outlook のサポートされているバージョンを持っていると想定できます。 ただし、OSC の現在のバージョンがクライアント コンピューター上にない場合は、配置コードことができますをダウンロードしてインストール、OSC の適切なバージョンで特別に構築した g ・ リンクの Url を使用して、 http://g.live.com。 これらの g ・ リンクは、バージョンと Outlook のビット数とクライアント コンピューターのロケールによって異なります。 G リンクを使用して、インストールしたり、OSC を更新する方法の詳細については、[インストールのチェックリスト](installation-checklist.md)を参照してください。
  
Outlook ユーザーは、OSC プロバイダーをインストールする前に、Outlook の OSC アドインを有効にするようにしてください。
  
OSC プロバイダーを展開する推奨される方法は、Windows インストーラー (.msi) パッケージを使用します。 各プロバイダーの展開機能を適切に確認するのには、次のシナリオをテストします。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|Outlook もは表示されません - Outlook 2003 または Outlook 2007 がインストールされていないと Outlook 2010 または Microsoft Outlook 2013 がインストールされていないがクイック実行で配信されました。  <br/> |展開が失敗します。  <br/> |
|Outlook 2003 または Outlook 2007 がインストールされていませんが、Outlook 2010 または Microsoft Outlook 2013 クイック実行で配信されました。  <br/> |32 ビット プロバイダーが配置されます。  <br/> |
|Outlook 2003 または Outlook 2007 がインストールされているが、OSC がインストールされていません。  <br/> |インストーラーのインストール、OSC とすべての修正プログラムです。 OSC が正常にインストールされた後、インストーラーは、プロバイダーを展開します。  <br/> |
|Outlook 2003 または Outlook 2007 がインストールされているし、OSC の以前のバージョンがインストールされています。  <br/> |インストーラーは、パッチへの g ・ リンク経由での OSC を更新し、プロバイダーが配置されます。  <br/> |
|Outlook 2003 または 2007 がインストールされているし、OSC が最新の状態です。  <br/> |インストーラーは、32 ビット プロバイダーを展開します。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013 がインストールされているが、OSC がインストールされていません。  <br/> |インストーラーは、適切なエラー メッセージで失敗します。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013 がインストールされているし、OSC の古いバージョンがインストールされています。  <br/> |インストールされている Outlook 2010 または Microsoft Outlook 2013 では、ビット数の適切なインストーラーでは、g ・ リンク経由で OSC が修正プログラム、更新し、適切なプロバイダーを展開し、します。  <br/> |
|Outlook 2010 または Microsoft Outlook 2013 がインストールされているし、OSC が最新の状態です。  <br/> |インストールされている Outlook 2010 (32 ビットまたは 64 ビット) の Microsoft Outlook 2013 のビット数の適切なインストーラーでは、適切なプロバイダーを展開します。  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>場所とレジストリ キーをインストール

OSC プロバイダーを展開した場所、ファイルの場所とは、プロバイダーのレジストリ キーが作成される Windows レジストリ内の場所を確認します。
  
### <a name="file-location-for-osc-provider-dlls"></a>OSC プロバイダー Dll のファイルの場所

次の表に記載されているシナリオをテストします。 デフォルトのインストール パスのテーブルは OSC プロバイダー Dll の一覧に注意してください。 ユーザーは、これらの Dll をインストールする場所をカスタマイズできます。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|Microsoft Outlook 2013 は、クライアント コンピューターにインストールされます。  <br/> |プロバイダー Dll は、Office15 フォルダーに配置されます。 オペレーティング システムは、64 ビットと 32 ビットは、Microsoft Outlook 2013、32 ビット Dll は、C:\Program Files (x86) の \Microsoft Office\Office15 の下で展開されます。 オペレーティング システムは、64 ビットと 64 ビットは、Microsoft Outlook 2013、C:\Program ファイル Office\Office15 で 64 ビットの Dll が配置されます。 オペレーティング システムが 32 ビットの場合は、Dll は、C:\Program ファイル Office\Office15 の下で展開されます。  <br/> |
|Outlook 2010 は、クライアント コンピューターにインストールされます。  <br/> |プロバイダー Dll は、Office14 フォルダーに配置されます。 オペレーティング システムは、64 ビットと、Outlook 2010 は、32 ビット、32 ビット Dll は、C:\Program Files (x86) の \Microsoft Office\Office14 の下で展開されます。 オペレーティング システムは、64 ビットと、Outlook 2010 は、64 ビット、64 ビットの Dll は、C:\Program ファイル Office\Office14 で展開されます。 オペレーティング システムが 32 ビットの場合は、Dll は、C:\Program ファイル Office\Office14 の下で展開されます。  <br/> |
|Outlook 2007 は、クライアント コンピューターにインストールされます。  <br/> |プロバイダー Dll は、C:\Program ファイル Office\Office14 の下に配置されます。 Office14 フォルダーを作成、OSC をインストールして、Dll は、任意のプロバイダーの前に、OSC をインストールする必要があります。 [Outlook の存在しクライアント コンピューター上の OSC](#olosc_TestingDeployment_PresenceOfOutlook)は、前のセクションを参照してください。  <br/> |
|Outlook 2003 は、クライアント コンピューターにインストールされます。  <br/> |プロバイダー Dll は、C:\Program ファイル Office\Office14 の下に配置されます。 Office14 フォルダーを作成、OSC をインストールして、Dll は、任意のプロバイダーの前に、OSC をインストールする必要があります。 [Outlook の存在しクライアント コンピューター上の OSC](#olosc_TestingDeployment_PresenceOfOutlook)は、前のセクションを参照してください。  <br/> |
|Microsoft Outlook 2013 いないがインストールされているが、クライアント コンピューター上でクイック実行で提供します。  <br/> |プロバイダー Dll は、Office15 フォルダーに配置されます。 オペレーティング システムが 64 ビット、32 ビットである場合、Dll は C:\Program Files (x86) \Microsoft Office\Office15 または C:\Program ファイル Office\Office15 の下で配置されます。 オペレーティング システムが 32 ビットの場合は、Dll は、C:\Program ファイル Office\Office15 の下で展開されます。 Office15 フォルダーが存在しない場合、インストールは、フォルダーを作成します。  <br/> |
|Outlook 2010 はないがインストールされているが、クライアント コンピューター上でクイック実行で提供。  <br/> |プロバイダー Dll は、Office14 フォルダーに配置されます。 オペレーティング システムが 64 ビット、32 ビットである場合、Dll は C:\Program Files (x86) \Microsoft Office\Office14 または C:\Program ファイル Office\Office14 の下で配置されます。 オペレーティング システムが 32 ビットの場合は、Dll は、C:\Program ファイル Office\Office14 の下で展開されます。 Office14 フォルダーが存在しない場合、インストールは、フォルダーを作成します。  <br/> |
   
### <a name="windows-registry-locations"></a>Windows レジストリの場所

次のことを確認します。
  
- OSC プロバイダーのインストーラーでは、いずれかの方法で、Windows レジストリに OSC プロバイダーの ProgID の値を作成`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`または`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。 
    
- 64 ビット Windows オペレーティング システムで実行されている 32 ビットの Outlook クライアント コンピューターにいるかどうかは例外です。 いずれかのプログラム Id を作成するこの例では、`HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`または`HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。
    
- レジストリ キーは同じである必要がある場合、regsvr32.exe を Dll を登録する代わりに、同じ場所にします。

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>インストールを削除します。

OSC プロバイダーのアンインストール処理が正常に動作することを確認するのにはいくつかのテストを次に示します。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|プロバイダーをアンインストールするのにを選択します。  <br/> |プロバイダーでは、Dll をアンインストールし、レジストリをクリアします。  <br/> |
|プロバイダーのアンインストール プロセスをキャンセルするユーザーを選択します。  <br/> |プロバイダーでは、アンインストール処理をキャンセルし、アンインストール処理を開始する前に、の状態に戻る、ユーザーは。  <br/> |
   
## <a name="see-also"></a>関連項目

- [プロバイダーを登録します。](registering-a-provider.md)  
- [インストールのチェックリスト](installation-checklist.md)
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)

