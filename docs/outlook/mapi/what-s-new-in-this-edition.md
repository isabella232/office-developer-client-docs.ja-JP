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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329548"
---
# <a name="whats-new-in-this-edition"></a>このエディションの新機能

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2013 MAPI リファレンスは、さまざまな新機能に関するドキュメントを含むように更新されています。 
  
## <a name="new-content"></a>新しいコンテンツ

コンテンツは、次の機能に対して追加されました。
  
- [outlook 2013 mapi リファレンスの作業の開始](getting-started-with-the-outlook-mapi-reference.md)に関するトピックは、outlook および mapi の機能のプログラミングモデルに関する総合的な情報を参照することによって更新され、最も多くの api とテクノロジを識別するのに役立ちます。必要に応じて。 参照されている技術記事へのリンクは、以下のトピックでも修正されています。 
    
  - [Outlook MAPI リファレンス](outlook-mapi-reference.md)
    
  - [Outlook MAPI ���t�@�����X�̊T�v](outlook-mapi-reference-overview.md)
    
- **メッセージストアプロバイダーの例**: ラップされた[PST ストアプロバイダーのサンプル](message-store-provider-sample.md)コードが、Outlook 2013 を認識して対応するように改訂されました。 詳細については、このトピックの「以前に改訂したコンテンツ」を参照してください。 
    
- **オートコンプリートストリーム**—以前は**Nk2 ファイル形式**である[ニックネームキャッシュ](nickname-cache.md)トピックが、outlook 2013 と outlook 2010 の変更を反映するように更新されています。 次のトピックが更新され、microsoft Outlook 2003/microsoft Office outlook 2007 およびバイナリファイル解析の nk2 ファイル形式の開発者ガイドラインに関する情報が提供されるようになりました。 詳細については、このトピックの「以前に改訂したコンテンツ」を参照してください。
    
  - [MAPI プロファイル](mapi-profiles.md)
    
  - [ニックネーム キャッシュ](nickname-cache.md)
    
  - [オートコンプリートストリーム](autocomplete-stream.md)
    
- **インターフェイス**- [IAddrBook:: openentry](iaddrbook-openentry.md)トピックには、アドレス帳エントリを開き、それにアクセスするために使用されるインターフェイスへのポインターを返すメソッドが記載されています。 以前は*ulflags*パラメーター **MAPI_GAL_ONLY**にフラグが含まれていました。これはグローバルアドレス一覧 (GAL) を開くために使用され、その定義を含むように変更されています。
    
- **プロパティ**— **PR_CONVERSATION_KEY**名前付きプロパティ ([PidTagConversationKey 標準プロパティ](pidtagconversationkey-canonical-property.md)) のトピックが追加され、IPM に関連してい**ます。MessageManager**メッセージは、Outlook MAPI のみで送信されます。 これに関連する以下のトピックと、トランスポート中立のカプセル化形式 (TNEF) ストリームのドキュメントが改訂されました。 
    
  - [標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
    
  - [MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)
    
  - [TNEF 属性から MAPI プロパティへのマッピング](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID and attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>以前に改訂されたコンテンツ

次の機能について、Outlook MAPI リファレンスの以前のリリースで追加されたコンテンツ。
  
- Microsoft Outlook 2013 では、並行して、またはクイック実行など、従来の展開シナリオでは使用できません。 これらのシナリオでは、適切な MAPI ライブラリの読み込みに使用されるロジックが複雑になることがあります。 mapi 開発者には、mapi 機能に明示的にリンクするオプションが用意されており、mapi ライブラリや Windows mapi スタブを経由することなく、既定の mapi クライアント (Outlook の Msmapi32 など) の mapi スタブに明示的にリンクすることを選択できます。 暗黙的リンクと比較した明示的なリンクの詳細については、「 [MAPI 関数へのリンク](how-to-link-to-mapi-functions.md)」を参照してください。 [CodePlex](https://mapistublibrary.codeplex.com/) web サイトに投稿された**mapi スタブライブラリ**は、32ビットと64ビットの両方の mapi アプリケーションのビルドをサポートする Mapi32 のためのドロップインリプレースを提供しています。 
    
- **64 ビット版 Microsoft Outlook のサポート**-適用可能な API 要素のリファレンストピックが、64ビットの outlook をサポートする新しいヘッダーファイルに対応するよう更新されました。 これらのヘッダーファイルは、 [Outlook 2010: MAPI ヘッダーファイル](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1)でダウンロードできます。 「 [outlook のバージョンを確認](how-to-check-the-version-of-outlook.md)する」で新しいコードサンプルが提供されました。インストールされている outlook のバージョンが64ビットの Microsoft outlook 2010 で、outlook 2013 用に更新されているかどうかを確認する方法について説明します。 既存の32ビット MAPI アプリケーションを、64ビットの Outlook がインストールされている64ビットのオペレーティングシステムで実行する場合は、32ビットアプリケーションを64ビットアプリケーションとして再構築する必要があります。 64ビット Outlook の mapi サポートの詳細については、「 [32 ビットおよび64ビットプラットフォームで mapi アプリケーションを作成](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)する」を参照してください。
    
- **メッセージストアプロバイダーの例**: ラップされた[PST ストアプロバイダーのサンプル](message-store-provider-sample.md)は、以前は64ビットアーキテクチャをサポートするように更新されていました。 「ラップされた pst[ストアプロバイダー](initializing-a-wrapped-pst-store-provider.md)の説明」の例では、「ラップされた pst および Unicode パス」に関する情報を提供するように展開されています。 
    
- **オートコンプリートストリーム**—以前は**Nk2 ファイル形式**である[ニックネームキャッシュ](nickname-cache.md)トピックが、outlook 2013 と outlook 2010 の変更を反映するように更新されました。 オートコンプリートリストなどの情報は、ユーザーが電子メールを作成している間**に [宛先**]、[ **Cc**]、および [ **Bcc** ] の各編集ボックスに表示される名前の一覧で、ローカルコンピューター上のメッセージの[オートコンプリートストリーム](autocomplete-stream.md)に保存されるようになりました。Outlook 2007 のようにファイルに保存するのではなく、ファイルに保存します。 
    
  - オートコンプリートストリームとの対話
    
  - オートコンプリートストリームを読み込む
    
  - オートコンプリートストリームの保存
    
- mapi クライアント**の高速シャットダウンのサポート**— mapi クライアントが迅速なシャットダウンを開始し、高速シャットダウンからのデータ損失を最小限にするために mapi サブシステムが読み込み済みプロバイダーに通知することができるようになりました。 高速シャットダウンをサポートするために、クライアントとプロバイダーに対して追加のインターフェイスが追加されました。 高速シャットダウンの詳細については、「 [MAPI でのクライアントのシャットダウン](client-shutdown-in-mapi.md)」を参照してください。
    
- **Outlook アイテムのフィールド定義のストリーム構造**— [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティのバイナリストリームのドキュメントが追加されました。 このプロパティは、Outlook アイテムの組み込みフィールドのすべてのユーザー設定フィールドおよびデータバインド設定の定義を指定します。 
    
- **個人ストアの上書き**-個人用フォルダーファイル (PST) ストアプロバイダー **PSTDisableGrow**ポリシーの上書きをサポートするために、次のインターフェイスとそれぞれのメソッドが追加されました。 
    
    [IPSTOVERRIDEREQ:: IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1:: IUnknown](ipstoverride1iunknown.md)
    
- **複数の Exchange アカウントを使用する**- [MAPI アドレス帳 API](using-multiple-exchange-accounts.md)のドキュメントが追加されました。 この API は、microsoft outlook 2010 で複数の Exchange アカウントをサポートするように強化され、microsoft outlook 2013 が含まれるようになりました。 ������ Exchange �A�J�E���g�Ő������A�h���X��������ɂ́A�A�h���X���ɒʘb�������� Exchange �A�J�E���g������ł���悤�ɁA�A�J�E���g�̃R���e�L�X�g���V�����@�\��g�p���܂��B 
    
- **mapi ファイル形式**— mapi 構成情報が拡張され、 [mapisvc.inf でのサービスおよびサービスプロバイダーの登録](registering-services-and-service-providers-in-mapisvc-inf.md)にパスを使用する方法を説明しました。
    
- **プロパティ**—次のタグ付きプロパティと、それまで追加されていた他のタグ付きプロパティと名前付きプロパティのドキュメントに加えて、次のタグ付きプロパティが追加されました。
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **mapi 定数**—統合[mapi 定数](mapi-constants.md)が展開されています。 以前のリリースでは、いくつかのトピックで配布されていましたが、1つのトピックで収集され、簡単に見つけて使用できるようになりました。 また、以下のセクションを含む、さらに広い範囲を提供するように拡張されました。 
    
  - Exchange アドレス帳およびメッセージストアのエラーコードの定義
    
  - Exchange Server メールボックスのキャッシュモードクォータの定義
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

