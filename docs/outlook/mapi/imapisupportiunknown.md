---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4843a52d7441de1e1ab545e80346db8dd308c4bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590205"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーおよびメッセージ サービスのエントリ ポイント関数では、通常実行するタスクの実装を提供します。 MAPI プロバイダー オブジェクトのログオン メソッドを呼び出すと、サービス プロバイダーからのサポートのオブジェクトへのポインターが表示されます。 メッセージ サービスでは、そのエントリ ポイント関数の呼び出しでのサポートのオブジェクト ポインターが表示されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって公開されます。  <br/> |サポート オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPISup  <br/> |
|ポインターの型。  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imapisupport-getlasterror.md) <br/> |以前のサポート オブジェクトのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |MAPI メモリの割り当てと割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |MAPI 経由の通知を受信するアドバイズ シンクを登録します。  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |**Subscribe**メソッドを呼び出して、以前に設定されている通知を送信するための責任をキャンセルします。  <br/> |
|[Notify](imapisupport-notify.md) <br/> |通知の**Subscribe**メソッドを最初に登録されたアドバイズ ソースに指定されたイベントの通知を送信します。  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |ステータス テーブルを変更するには、新しい行を追加したり、既存の行を変更します。  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |トランスポート プロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造体を作成します。  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |オブジェクトを使用不可としてマークを付けます。  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |必要と見なされるすべてのタスクを実行できるように、MAPI スプーラーを CPU の制御を提供します。  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |またはサービスの要求のステータスが変更された、MAPI スプーラーに通知します。  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |一時アドレスのエントリ id を作成します。  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |サービス プロバイダーを一意に表す**MAPIUID**構造体を登録します。  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |外部のアドレス帳で受信者のエントリが表示されます。  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするためのインターフェイス ポインターを返します。  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |MAPI の一時テーブル (すべてのアドレスが新しい受信者を作成するためのサポートについてプロバイダーを登録しているテンプレートの一覧) へのポインターを返します。  <br/> |
|[住所](imapisupport-address.md) <br/> |共通のアドレス] ダイアログ ボックスが表示されます。  <br/> |
|[詳細](imapisupport-details.md) <br/> |特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |アドレス帳コンテナーに直接、または送信メッセージの受信者の一覧には、新しい受信者を追加します。  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |構成のプロパティ シートを表示します。  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |別のフォルダーに 1 つのフォルダーからのコピーや移動メッセージです。  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |現在の親フォルダーから別の親フォルダーにフォルダーを移動またはコピーします。  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |明確に除外されたプロパティを 1 つのオブジェクトのすべてのプロパティを別のオブジェクトを移動またはコピーします。  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |オブジェクトの 1 つまたは複数のプロパティを別のオブジェクトを移動またはコピーします。  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |進行状況インジケーターを表示する進行中のオブジェクトを取得します。  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |読み取りまたはメッセージの nonread のレポートを生成します。  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |MAPI スプーラーに送信するためには、メッセージを準備します。  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |メッセージの受信者リスト、特定の配布リストの展開を完了します。  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |���M���ꂽ���b�Z�[�W��������܂��B  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |アドレス帳へのアクセスを提供します。  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |メッセージのポスト プロセスを実行します。  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |メッセージ ストアの正常型解放を要求します。  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |配信し、配信不能レポートを生成します。  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |MAPI の標準的な形式のエントリ id をメッセージ ・ ストアの内部のエントリの識別子に変換します。  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |永続的なプロファイルのセクションを保存するメッセージを変更します。  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |ストリームにアクセスするためのストレージ オブジェクトを実装します。  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |メッセージ サービスのサポート オブジェクトを作成します。  <br/> |
   
## <a name="remarks"></a>注釈

書籍、メッセージ ・ ストア、トランスポート プロバイダー、および各サービスは、独自のサポート オブジェクトを持つメッセージに対応します。 サービス プロバイダーおよびメッセージ サービスは、他のインターフェイス メソッドの実装の一部としてサポート オブジェクトでメソッドを呼び出します。 各サポートのさまざまなオブジェクトには、呼び出し元に適用する方法の完全な実装適用されているメソッドは、MAPI_E_NO_SUPPORT を返します。 アドレス帳プロバイダーのサポート オブジェクトでは、次のメソッドの実装を持ちます。
  
||||
|:-----|:-----|:-----|
|**住所** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**詳細** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**発生しました** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
メッセージ ストア プロバイダーのサポートのオブジェクトでは、次のメソッドの実装を持ちます。
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**発生しました** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
トランスポート プロバイダーのサポートのオブジェクトでは、次のメソッドの実装を持ちます。
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**発生しました** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
   
メッセージ サービスのサポート対象では、次のメソッドの実装を持ちます。
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**発生しました** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

