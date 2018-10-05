---
title: このエディションの新機能
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392887"
---
# <a name="whats-new-in-this-edition"></a>このエディションの新機能

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
さまざまな新機能のマニュアルを含めるため、Microsoft Outlook 2013 MAPI の参照が更新されました。 
  
## <a name="new-content"></a>新しいコンテンツ

次の機能に関するコンテンツが追加されました。
  
- プログラミング モデルの Api とは、多くのテクノロジを識別するために、Outlook と MAPI の機能についての包括的な情報を参照する[Outlook 2013 の MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)のトピックが更新されましたお客様のニーズに適しています。 技術資料へのリンクは、以下のトピックも更新されています。 
    
  - [Outlook MAPI リファレンス](outlook-mapi-reference.md)
    
  - [Outlook MAPI リファレンス概要](outlook-mapi-reference-overview.md)
    
- **メッセージ ストア プロバイダーの例**などを認識し、Outlook 2013 に対応する[PST ストア プロバイダーのラップのサンプル](message-store-provider-sample.md)コードが変更されたようになりました。 詳細については、このトピックで以前修正されたコンテンツを参照してください。 
    
- **オートコンプリートのストリーム**[ニックネームのキャッシュ](nickname-cache.md)のトピック、以前、 **Nk2 ファイル形式**、Outlook 2013 と、Outlook 2010 での変更を反映するように更新されました。 次のトピックは、Microsoft Outlook 2003 と Microsoft Office Outlook 2007 およびバイナリ ファイルの解析の .nk2 ファイル形式の開発者のガイドラインについての情報を提供するよう更新されています。 詳細については、このトピックで以前修正されたコンテンツを参照してください。
    
  - [MAPI プロファイル](mapi-profiles.md)
    
  - [ニックネーム キャッシュ](nickname-cache.md)
    
  - [オートコンプリート ストリーム](autocomplete-stream.md)
    
- **インタ フェース**の[アドレス帳コンテナー](iaddrbook-openentry.md)のトピックでのエントリをアドレス帳を開くと、それにアクセスするためのインターフェイスにポインターを返すメソッドについて説明します。 **MAPI_GAL_ONLY**を開くには、グローバル アドレス一覧 (GAL) でのみ、使用する可能性があり、その定義を含むように改訂されている*ulFlags*パラメーターのフラグが含まれていた。
    
- **プロパティ**-プロパティ ([PidTagConversationKey の標準的なプロパティ](pidtagconversationkey-canonical-property.md)のトピックを名前付きの**PR_CONVERSATION_KEY**が追加され、IPM の**に関連しています。MessageManager** Outlook MAPI でのメッセージのみです。 トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのドキュメントに関連する次のトピックが更新されています。 
    
  - [標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
    
  - [MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)
    
  - [TNEF の属性から MAPI プロパティへのマッピング](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID and attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>以前の改訂内容

コンテンツは、Outlook MAPI の参照の次の機能の以前のリリースで追加されました。
  
- Microsoft Outlook 2013 は、サイド バイ サイドやクイック実行などの従来の展開シナリオになります。 これらのシナリオには、適切な MAPI ライブラリをロードするためのロジックが複雑になることができます。 MAPI 開発者は、MAPI の関数を明示的にリンクすることが今すぐと MAPI ライブラリと Windows の MAPI スタブを経由せずに既定の MAPI クライアント (たとえば、Msmapi32.dll の Outlook の MAPI スタブを明示的にリンクを選択できます。 暗黙的なリンクと明示的なリンクの詳細については、 [MAPI の関数へのリンク](how-to-link-to-mapi-functions.md)を参照してください。 **MAPI スタブ ライブラリ**、 [CodePlex](https://mapistublibrary.codeplex.com/)の web サイトに掲載は、32 ビットと 64 ビットの両方の MAPI アプリケーションの構築をサポートする Mapi32.lib のドロップイン交換を提供します。 
    
- **64 ビットの Microsoft Outlook のサポート**64 ビットの Outlook をサポートする新しいヘッダー ファイルに対応するように該当する API 要素のリファレンス トピックが更新されました。 これらのヘッダー ファイルはダウンロードとして利用可能な[Outlook 2010: MAPI ヘッダー ファイル](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1)です。 インストールされているバージョンの Outlook が Microsoft Outlook 2010 の 64 ビットであり、Outlook 2013 が改訂されたかどうかを確認する方法を表示する[Outlook のバージョンを確認](how-to-check-the-version-of-outlook.md)ので、新しいコード サンプルが提供されました。 既存の 32 ビットの MAPI アプリケーションがインストールされている 64 ビットの Outlook を 64 ビット オペレーティング システムで実行されている場合は、64 ビット アプリケーションと 32 ビット アプリケーションを再構築する必要があります。 64 ビットの Outlook の MAPI サポートの詳細については、 [32 ビットと 64 ビット プラットフォーム上の MAPI アプリケーションの構築](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)を参照してください。
    
- **メッセージ ストア プロバイダーの例**: 64 ビット アーキテクチャをサポートするために以前更新された[サンプル PST ストア プロバイダーをラップ](message-store-provider-sample.md)します。 例の[ラップの PST ストア プロバイダーの初期化中](initializing-a-wrapped-pst-store-provider.md)のトピックは、「Wrapped PST と Unicode パス」情報を提供するよう拡張されて 
    
- **オートコンプリートのストリーム**[ニックネームのキャッシュ](nickname-cache.md)のトピック、以前、 **Nk2 ファイル形式**、Outlook 2013 と、Outlook 2010 での変更を反映するように更新されました。 ローカル コンピューターでメッセージの[ストリームのオートコンプリート](autocomplete-stream.md)には、ユーザーが電子メールを作成するとき**に** **[cc]**、および **[bcc]** 編集ボックスで表示される名前の一覧で、オートコンプリートの一覧などの情報が保存されます。せず Outlook 2007 のようにファイルに保存します。 
    
  - オートコンプリートのストリームを操作します。
    
  - オートコンプリートのストリームの読み込み
    
  - オートコンプリートのストリームを保存します。
    
- **MAPI クライアント用の高速シャット ダウンのサポート**: MAPI クライアントがこれですばやくシャット ダウンを開始し、高速シャット ダウンからのデータの損失を最小限に抑えるために読み込まれているプロバイダーに通知する MAPI サブシステムがあります。 高速シャット ダウンをサポートするためにクライアントとプロバイダーの追加のインターフェイスが追加されました。 高速シャット ダウンの詳細については、 [mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)を参照してください。
    
- **Outlook アイテムのフィールド定義のストリームの構造体**、 [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティのバイナリ ストリームのドキュメントが追加されました。 このプロパティは、すべてのユーザー設定フィールドと組み込みの Outlook アイテムのフィールドのデータ バインディングの設定の定義を指定します。 
    
- **個人ストアを上書き**: 個人用フォルダー ファイル (PST) のストア プロバイダー **PSTDisableGrow**ポリシーをオーバーライドすることをサポートするために、次のインターフェイスと、それぞれのメソッドが追加されました。 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **複数の Exchange アカウントを使用して**、 [MAPI アドレス帳の API](using-multiple-exchange-accounts.md)のドキュメントが追加されました。 この API は、Microsoft Outlook 2010 で複数の Exchange アカウントをサポートするために拡張された、Microsoft Outlook 2013 が含まれています。 ������ Exchange �A�J�E���g�Ő������A�h���X��������ɂ́A�A�h���X���ɒʘb�������� Exchange �A�J�E���g������ł���悤�ɁA�A�J�E���g�̃R���e�L�X�g���V�����@�\��g�p���܂��B 
    
- **MAPI ファイルの形式**: MAPI 構成情報は、[サービスを登録し MapiSvc.inf のサービス プロバイダー](registering-services-and-service-providers-in-mapisvc-inf.md)のパスを使用する方法を説明するため拡張されています。
    
- **プロパティ**: 38 その他のプロパティをタグ付けし、名前付きプロパティが追加されているドキュメントだけでなく、次のタグ付きのプロパティが追加されました。
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI 定数**: 統合された[MAPI 定数](mapi-constants.md)が展開されています。 以前のリリースでは、トピック数で配布されましたが、1 つのトピックの検索および使用しやすくするために収集されるようになりました。 次のセクションを含むより広範なカバレッジを提供する展開されてもいます。 
    
  - Exchange アドレス帳とメッセージ ・ ストアのエラー コードの定義
    
  - Exchange Server メールボックスの定義がキャッシュ モードのクォータ
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

