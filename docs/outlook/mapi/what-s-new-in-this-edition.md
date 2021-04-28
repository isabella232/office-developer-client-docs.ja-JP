---
title: このエディションの新機能
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '最終更新日: 2020 年 2 月 9 日'
ms.openlocfilehash: 3a3d38d83311b63686a2379c3321194e538ff840
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061329"
---
# <a name="whats-new-in-this-edition"></a>このエディションの新機能

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft OUTLOOK MAPI リファレンスが更新され、さまざまな新機能に関するドキュメントが含まれています。 
  
## <a name="new-content"></a>新しいコンテンツ

次の機能のコンテンツが追加されました。
  
- トピック[Outlook 2013 MAPI](getting-started-with-the-outlook-mapi-reference.md)リファレンスの概要が更新され、Outlook および MAPI 機能のプログラミング モデルに関する包括的な情報が参照され、ニーズに最も適した API とテクノロジを特定できます。 参照されている技術記事へのリンクも、次のトピックで改訂されています。 
    
  - [Outlook MAPI リファレンス](outlook-mapi-reference.md)
    
  - [Outlook MAPI ���t�@�����X�̊T�v](outlook-mapi-reference-overview.md)
    
- **メッセージ ストア プロバイダーの例**—2013 年にラップされた [PST](message-store-provider-sample.md)ストア プロバイダーのサンプル コードが認識され、対応Outlookされました。 詳細については、このトピックの「以前に改訂されたコンテンツ」を参照してください。 
    
- **Autocomplete Stream**—[ニックネーム](nickname-cache.md)キャッシュ トピック (以前は **Nk2** ファイル形式) は、Outlook 2013 および Outlook 2010 の変更を反映するように更新されました。 次のトピックは、Microsoft Outlook 2003/Microsoft Office Outlook 2007 およびバイナリ ファイル解析の .nk2 ファイル形式開発者向けガイドラインに関する情報を提供するために改訂されました。 詳細については、このトピックの「以前に改訂されたコンテンツ」を参照してください。
    
  - [MAPI プロファイル](mapi-profiles.md)
    
  - [ニックネーム キャッシュ](nickname-cache.md)
    
  - [オートコンプリート ストリーム](autocomplete-stream.md)
    
- **Interfaces** [-IAddrBook::OpenEntry](iaddrbook-openentry.md) トピックでは、アドレス帳エントリを開き、アドレス帳エントリへのアクセスに使用するインターフェイスへのポインターを返す方法について説明します。 以前は  *ulFlags*  パラメーター **MAPI_GAL_ONLY** にフラグが含まれているので、グローバル アドレス一覧 (GAL) のみを開く場合に使用し、その定義を含める変更が行いました。
    
- **Properties** **—PR_CONVERSATION_KEYプロパティ**[(PidTagConversationKey](pidtagconversationkey-canonical-property.md)標準プロパティ) トピックが追加され **、IPM に関連付けされています。MAPI 内の MessageManager** Outlookのみ。 関連する以下のトピックと、Transport-Neutralカプセル化形式 (TNEF) ストリームのドキュメントが改訂されました。 
    
  - [標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
    
  - [MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)
    
  - [TNEF 属性と MAPI プロパティのマッピング](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID and attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>MAPI 初期化モニター  

- MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。 たとえば、MAPI を初期化できる複数のスレッドがある場合や、アプリケーションの初期化中に MAPI が初期化された場合は、何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。  初期化モニターは、関数 (OLMAPI32.DLL からエクスポート) と、以下に示すいくつかの簡単なインターフェイスを使用して、この機能を提供します。 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor) 

- これは、OLMAPI32.DLL からエクスポートされたエントリ ポイントです。これにより、呼び出し元はインターフェイスを取得して現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。  この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。  また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。 COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。 

### <a name="interface-imapiinitmonitor"></a>インターフェイス: IMAPIInitMonitor 

**IFACEMETHODIMP_(BOOL) IsInitialized()**
- MAPI の初期化の現在の状態を返します。 

**IFACEMETHODIMP Wait(DWORD タイムアウト)**
- このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。  INFINITE は、無限の待機に使用できます。 

**IFACEMETHODIMP BeginWait(DWORD タイムアウト、IMAPIWaitResult ppResult)**
- MAPI の初期化または指定した経過時間 (ミリ秒単位) の待機を開始します。   これにより、IMAPIWaitResult インターフェイスが返され、待機を開始するために "End" が呼び出される必要があります。  これにより、呼び出し元は、待機中にブロックされるスレッドを制御できます。 

### <a name="interface-imapiwaitresult"></a>インターフェイス IMAPIWaitResult
**IFACEMETHODIMP End() オーバーライド**
- スレッドが呼び出されるスレッドでブロック待機を開始するために呼び出され、"BeginWait" と呼ばれるスレッドである必要があります。 

    
## <a name="previously-revised-content"></a>以前に変更されたコンテンツ

コンテンツは、MAPI リファレンスの以前のリリースOutlook次の機能で追加されました。
  
- Microsoft Outlook 2013を使用すると、サイド バイ サイドやアプリケーションなどの従来の展開シナリオクイック実行。 これらのシナリオでは、適切な MAPI ライブラリの読み込みに使用されるロジックが複雑になります。 MAPI 開発者は、MAPI 関数に明示的にリンクするオプションを持ち、MAPI ライブラリと Windows MAPI スタブを経由せずに、既定の MAPI クライアント (Outlook の Msmapi32.dll など) の MAPI スタブに明示的にリンクすることができます。 暗黙的なリンクと比較した明示的なリンクの詳細については、「MAPI 関数へのリンク [」を参照してください](how-to-link-to-mapi-functions.md)。 [CodePlex](https://mapistublibrary.codeplex.com/) Web サイトに投稿された **MAPI** スタブ ライブラリは、32 ビット MAPI アプリケーションと 64 ビット MAPI アプリケーションの両方の構築をサポートする Mapi32.lib のドロップイン置換を提供します。 
    
- **64** ビット Microsoft Outlook のサポート -適用可能な API 要素のリファレンス トピックが更新され、64 ビット バージョンをサポートする新しいヘッダー ファイルに対応Outlook。 これらのヘッダー ファイルは[、2010 年 2010](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1)年Outlook MAPI ヘッダー ファイルでダウンロードできます。 Outlook のバージョンを確認して[](how-to-check-the-version-of-outlook.md)、インストールされているバージョンの Outlook が 64 ビット Microsoft Outlook 2010 であるかどうかを確認する方法を示す新しいコード サンプルが提供され、Outlook 2013 年に改訂されました。 64 ビット Outlook がインストールされている 64 ビット オペレーティング システムで既存の 32 ビット MAPI アプリケーションを実行する場合は、64 ビット アプリケーションとして 32 ビット アプリケーションを再構築する必要があります。 64 ビット の MAPI サポートの詳細[Outlook、32 ビットおよび 64 ビット](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)プラットフォームでの MAPI アプリケーションの構築を参照してください。
    
- **メッセージ ストア プロバイダーの例**:ラップ [された PST](message-store-provider-sample.md) ストア プロバイダーのサンプルは、64 ビットアーキテクチャをサポートするために以前に更新されました。 この例の「ラップ [された PST](initializing-a-wrapped-pst-store-provider.md) ストア プロバイダーの初期化」トピックが展開され、「ラップされた PST と Unicode パス」に関する情報が提供されました。 
    
- **Autocomplete Stream**—[ニックネーム](nickname-cache.md)キャッシュ トピック (以前は **Nk2 ファイル** 形式) が更新され、Outlook 2013 および Outlook 2010 の変更が反映されています。 ユーザーが電子メールを作成している間に [To] **、Cc、****および Bcc** の編集ボックスに表示される名前の一覧であるオートコンプリート リストなどの情報は、Outlook 2007 のようにファイルに保存するのではなく、ローカル コンピューター上のメッセージのオートコンプリート ストリームに保存されます。  [](autocomplete-stream.md) 
    
  - オートコンプリート ストリームの操作
    
  - オートコンプリート ストリームの読み込み
    
  - オートコンプリート ストリームの保存
    
- **MAPI クライアントの高速シャットダウン** のサポート —MAPI クライアントは、クイック シャットダウンを開始し、MAPI サブシステムに読み込まれたプロバイダーに通知して、高速シャットダウンによるデータ損失を最小限に抑えます。 クライアントとプロバイダーが高速シャットダウンをサポートするために追加のインターフェイスが追加されました。 高速シャットダウンの詳細については [、「MAPI でのクライアント シャットダウン」を参照してください](client-shutdown-in-mapi.md)。
    
- **アイテムのフィールド** 定義Outlookストリーム構造 [-PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティのバイナリ ストリームのドキュメントが追加されました。 このプロパティは、すべてのユーザー設定フィールドの定義と、ユーザー設定アイテムの組み込みフィールドのデータ バインドOutlookします。 
    
- **個人用ストアの上書** き —個人用フォルダー ファイル (PST) ストア プロバイダー **PSTDisableGrow** ポリシーのオーバーライドをサポートするために、次のインターフェイスとそれぞれのメソッドが追加されました。 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **複数のExchangeアカウントを使用** する [—MAPI アドレス](using-multiple-exchange-accounts.md)帳 API のドキュメントが追加されました。 この API は、複数のアカウントをサポートExchange強化され、Microsoft Outlook 2010が含Microsoft Outlook 2013。 ������ Exchange �A�J�E���g�Ő������A�h���X��������ɂ́A�A�h���X���ɒʘb�������� Exchange �A�J�E���g������ł���悤�ɁA�A�J�E���g�̃R���e�L�X�g���V�����@�\��g�p���܂��B 
    
- **MAPI ファイル形式**—MAPI 構成情報が展開され [、MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md)のサービスとサービス プロバイダーの登録でパスを使用する方法が説明されています。
    
- **Properties**—以前に追加された 38 の他のタグ付きプロパティと名前付きプロパティのドキュメントに加えて、次のタグ付きプロパティが追加されました。
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI 定数**—統合 [MAPI 定数が](mapi-constants.md) 拡張されました。 以前のリリースでは、複数のトピックで配布されましたが、1 つのトピックで収集され、検出と使用が容易になりました。 また、次のセクションを含む、より広範な範囲を提供するために拡張されています。 
    
  - アドレス帳Exchangeメッセージ ストアのエラー コードの定義
    
  - メールボックス キャッシュ Exchange Serverクォータの定義
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

