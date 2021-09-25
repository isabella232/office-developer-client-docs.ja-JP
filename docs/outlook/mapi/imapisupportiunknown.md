---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ad54ca8efccebd28ed38ebd457fb258a3f59790
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625393"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーおよびメッセージ サービス エントリ ポイント関数によって通常実行されるタスクの実装を提供します。 MAPI がプロバイダー オブジェクトのログオン メソッドを呼び出す場合、サービス プロバイダーはサポート オブジェクトへのポインターを受け取る。 メッセージ サービスは、エントリ ポイント関数の呼び出しでサポート オブジェクト ポインターを受け取ります。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|次のユーザーによって公開されます。  <br/> |サポート オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISup  <br/> |
|ポインターの種類:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |以前のサポート オブジェクト エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |MAPI メモリ割り当ておよび割り当て解除関数[(MAPIAllocateBuffer、MAPIAllocateMore、および](mapiallocatemore.md) [MAPIFreeBuffer)](mapifreebuffer.md)のアドレスを取得します。[](mapiallocatebuffer.md)  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |MAPI 経由で通知を受け取るアドバイス シンクを登録します。  <br/> |
|[登録を解除する](imapisupport-unsubscribe.md) <br/> |Subscribe メソッドの呼び出しで以前に確立された通知の送信の責任を **取り消** します。  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Subscribe メソッドを使用して、指定したイベントの通知を、最初に通知用に登録されたアドバイス ソースに **送信** します。  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |新しい行を追加するか、既存の行を変更して、状態テーブルを変更します。  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |トランスポート プロバイダーのプリプロセッサ関数 [(PreprocessMessage](preprocessmessage.md) プロトタイプに準拠する関数) を登録します。  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |一意の [識別子として使用する新しい MAPIUID](mapiuid.md) 構造を作成します。  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |オブジェクトを使用不可としてマークします。  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |MAPI スプーラーに CPU を制御し、必要と見なされるタスクを実行できます。  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |状態の変更またはサービスの要求を MAPI スプーラーに通知します。  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |1 回のアドレスのエントリ識別子を作成します。  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |サービス プロバイダーを **一意に表す MAPIUID** 構造体を登録します。  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |外部アドレス帳プロバイダーで受信者エントリを開きます。  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |MAPI 一時テーブルへのポインター (すべてのアドレス帳プロバイダーが新しい受信者の作成をサポートするテンプレートの一覧) を返します。  <br/> |
|[Address](imapisupport-address.md) <br/> |[共通アドレス] ダイアログ ボックスを表示します。  <br/> |
|[詳細](imapisupport-details.md) <br/> |特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |アドレス帳コンテナーまたは送信メッセージの受信者リストに、新しい受信者を直接追加します。  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |構成プロパティ シートを表示します。  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |メッセージを 1 つのフォルダーから別のフォルダーにコピーまたは移動します。  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |現在の親フォルダーから別の親フォルダーにフォルダーをコピーまたは移動します。  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |特定の除外プロパティを除く、1 つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |オブジェクトの 1 つ以上のプロパティを別のオブジェクトにコピーまたは移動します。  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |進行状況インジケーターを表示する進行状況オブジェクトを取得します。  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |メッセージの読み取りまたは読み取り以外のレポートを生成します。  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |MAPI スプーラーに送信するメッセージを準備します。  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |メッセージの受信者リストを完了し、特定の配布リストを展開します。  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |���M���ꂽ���b�Z�[�W��������܂��B  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |アドレス帳へのアクセスを提供します。  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |メッセージに対して後処理を実行します。  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |メッセージ ストアの順序付きリリースを要求します。  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |配信レポートと配信以外のレポートを生成します。  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |メッセージ ストアの内部エントリ識別子を MAPI 標準形式のエントリ識別子に変換します。  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |メッセージ ストア のプロファイル セクションを永続的に変更します。  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |ストリームにアクセスするストレージ オブジェクトを実装します。  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |メッセージ サービスサポート オブジェクトを作成します。  <br/> |
   
## <a name="remarks"></a>注釈

アドレス帳、メッセージ ストア、トランスポート プロバイダー、およびメッセージ サービスには、それぞれ独自のサポート オブジェクトがあります。 サービス プロバイダーとメッセージ サービスは、他のインターフェイス メソッドの実装の一環として、サポート オブジェクト内のメソッドを呼び出します。 各サポート オブジェクトには、呼び出し元に適用されるメソッドの完全な実装があります。適用可能ではないメソッドは、MAPI_E_NO_SUPPORT。 アドレス帳プロバイダーのサポート オブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**Address** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**詳細** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**登録を解除する** <br/> |**WrapStoreEntryID** <br/> |
   
メッセージ ストア プロバイダーのサポート オブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**登録を解除する** <br/> |
|**WrapStoreEntryID** <br/> |
   
トランスポート プロバイダーのサポート オブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**登録を解除する** <br/> |
   
メッセージ サービス サポート オブジェクトには、次のメソッドの実装があります。
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

