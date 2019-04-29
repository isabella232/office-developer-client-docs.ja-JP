---
title: imapisupport IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415440"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常はサービスプロバイダーとメッセージサービスエントリポイント関数によって実行されるタスクの実装を提供します。 サービスプロバイダーは、MAPI がプロバイダーオブジェクトのログオン方法を呼び出している場合、サポートオブジェクトへのポインターを受け取ります。 メッセージサービスは、そのエントリポイント関数の呼び出しで、サポートオブジェクトポインターを受け取ります。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|公開者:  <br/> |サポートオブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISup  <br/> |
|ポインターの種類:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |以前のサポートオブジェクトエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[getmemallocroutines](imapisupport-getmemallocroutines.md) <br/> |MAPI メモリ割り当て関数および割り当て解除関数 ([MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)) のアドレスを取得します。  <br/> |
|[こう](imapisupport-subscribe.md) <br/> |通知を MAPI 経由で受信するようにアドバイズシンクを登録します。  <br/> |
|[登録を解除する](imapisupport-unsubscribe.md) <br/> |**Subscribe**メソッドの呼び出しによって以前に確立された通知を送信する責任を取り消します。  <br/> |
|[Notify](imapisupport-notify.md) <br/> |指定したイベントの通知を、 **Subscribe**メソッドによって最初に通知用に登録したアドバイズソースに送信します。  <br/> |
|[modifystatusrow](imapisupport-modifystatusrow.md) <br/> |新しい行を追加するか、または既存の行を変更して、状態テーブルを変更します。  <br/> |
|[openプロファイル '](imapisupport-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md) <br/> |トランスポートプロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。  <br/> |
|[newuid](imapisupport-newuid.md) <br/> |一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造を作成します。  <br/> |
|[makeinvalid](imapisupport-makeinvalid.md) <br/> |オブジェクトを使用不可としてマークします。  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |MAPI スプーラーに CPU を制御します。これにより、必要なタスクを実行できるようになります。  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |状態の変更またはサービスの要求の MAPI スプーラーに通知します。  <br/> |
|[createoneoff](imapisupport-createoneoff.md) <br/> |1回限りのアドレスのエントリ id を作成します。  <br/> |
|[setprovideruid](imapisupport-setprovideruid.md) <br/> |サービスプロバイダーを一意に表す**MAPIUID**構造体を登録します。  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |外部アドレス帳プロバイダーの受信者エントリを開きます。  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。  <br/> |
|[getoneofftable](imapisupport-getoneofftable.md) <br/> |MAPI の1回限りのテーブルへのポインター (すべてのアドレス帳プロバイダーが新しい受信者を作成するためにサポートするテンプレートのリスト) を返します。  <br/> |
|[住所](imapisupport-address.md) <br/> |[共通のアドレス] ダイアログボックスを表示します。  <br/> |
|[詳細](imapisupport-details.md) <br/> |特定のアドレス帳エントリの詳細を表示するダイアログボックスを表示します。  <br/> |
|[newentry](imapisupport-newentry.md) <br/> |アドレス帳コンテナーまたは送信メッセージの受信者リストに、新しい受信者を直接追加します。  <br/> |
|[doconfigpropsheet](imapisupport-doconfigpropsheet.md) <br/> |構成プロパティシートを表示します。  <br/> |
|[copymessages](imapisupport-copymessages.md) <br/> |メッセージを1つのフォルダーから別のフォルダーにコピーまたは移動します。  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |フォルダーを現在の親フォルダーから別の親フォルダーにコピーまたは移動します。  <br/> |
|[docopyto](imapisupport-docopyto.md) <br/> |明示的に除外されたプロパティを除き、1つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。  <br/> |
|[docopyprops](imapisupport-docopyprops.md) <br/> |オブジェクトの1つまたは複数のプロパティを別のオブジェクトにコピーまたは移動します。  <br/> |
|[do進捗ダイアログ](imapisupport-doprogressdialog.md) <br/> |進行状況インジケーターを表示する progress オブジェクトを取得します。  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |メッセージの読み取りまたは非開封レポートを生成します。  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |MAPI スプーラーに送信するためのメッセージを準備します。  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |特定の配布リストを展開し、メッセージの受信者の一覧を完成させる。  <br/> |
|[do送信メール](imapisupport-dosentmail.md) <br/> |���M���ꂽ���b�Z�[�W��������܂��B  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |アドレス帳へのアクセスを提供します。  <br/> |
|[すべてのアウトの sg](imapisupport-completemsg.md) <br/> |メッセージに対して後処理を実行します。  <br/> |
|[storelogofftransports](imapisupport-storelogofftransports.md) <br/> |メッセージストアの正常なリリースを要求します。  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |配信レポートおよび配信不能レポートを生成します。  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |メッセージストアの内部エントリ識別子を MAPI 標準形式のエントリ id に変換します。  <br/> |
|[modifyprofile](imapisupport-modifyprofile.md) <br/> |メッセージストアプロファイルセクションの変更を永続的に行います。  <br/> |
|[istoragefromstream](imapisupport-istoragefromstream.md) <br/> |stream にアクセスするためのストレージオブジェクトを実装します。  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |メッセージサービスサポートオブジェクトを作成します。  <br/> |
   
## <a name="remarks"></a>注釈

各アドレス帳、メッセージストア、トランスポートプロバイダー、およびメッセージサービスには、それぞれ独自のサポートオブジェクトがあります。 サービスプロバイダーとメッセージサービスは、他のインターフェイスメソッドの実装の一部として、サポートオブジェクト内のメソッドを呼び出します。 それぞれの異なるサポートオブジェクトには、呼び出し元に適用されるメソッドの実装が完全に実装されています。該当しないメソッドは MAPI_E_NO_SUPPORT を返します。 アドレス帳プロバイダーのサポートオブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**住所** <br/> |**CompareEntryIDs** <br/> |**createoneoff** <br/> |
|**詳細** <br/> |**doconfigpropsheet** <br/> |**do進捗ダイアログ** <br/> |
|**GetLastError** <br/> |**getmemallocroutines** <br/> |**getoneofftable** <br/> |
|**istoragefromstream** <br/> |**GetSvcConfigSupportObj** <br/> |**makeinvalid** <br/> |
|**modifystatusrow** <br/> |**newentry** <br/> |**newuid** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**openプロファイル '** <br/> |**OpenTemplateID** <br/> |**setprovideruid** <br/> |
|**こう** <br/> |**登録を解除する** <br/> |**WrapStoreEntryID** <br/> |
   
メッセージストアプロバイダーのサポートオブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**すべてのアウトの sg** <br/> |**CopyFolder** <br/> |
|**copymessages** <br/> |**createoneoff** <br/> |**docopyprops** <br/> |
|**docopyto** <br/> |**doconfigpropsheet** <br/> |**do進捗ダイアログ** <br/> |
|**do送信メール** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**getmemallocroutines** <br/> |**GetSvcConfigSupportObj** <br/> |**makeinvalid** <br/> |
|**istoragefromstream** <br/> |**modifyprofile** <br/> |**modifystatusrow** <br/> |
|**newuid** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**openプロファイル '** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**setprovideruid** <br/> |**SpoolerNotify** <br/> |
|**storelogofftransports** <br/> |**こう** <br/> |**登録を解除する** <br/> |
|**WrapStoreEntryID** <br/> |
   
トランスポートプロバイダーのサポートオブジェクトには、次のメソッドの実装があります。
  
||||
|:-----|:-----|:-----|
|**doconfigpropsheet** <br/> |**CompareEntryIDs** <br/> |**createoneoff** <br/> |
|**getmemallocroutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**istoragefromstream** <br/> |**makeinvalid** <br/> |**modifystatusrow** <br/> |
|**OpenAddressBook** <br/> |**registerpreprocessor プロセッサ** <br/> |**newuid** <br/> |
|**Notify** <br/> |**openプロファイル '** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**こう** <br/> |**登録を解除する** <br/> |
   
メッセージサービスサポートオブジェクトには、次のメソッドの実装があります。
  
|||
|:-----|:-----|
|**doconfigpropsheet** <br/> |**GetLastError** <br/> |
|**getmemallocroutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**makeinvalid** <br/> |**newuid** <br/> |
|**openプロファイル '** <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

