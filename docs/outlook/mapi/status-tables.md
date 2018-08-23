---
title: 状態テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: afbef333af46051284fa51d52c2e3f77607b0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804016"
---
# <a name="status-tables"></a>状態テーブル

  
  
**適用対象**: Outlook 
  
ステータス テーブルには、現在のセッションの状態に関連する情報が含まれています。 MAPI とサービス ・ プロバイダーによって提供される情報が含まれるすべての MAPI セッションの状態の 1 つのテーブルがあります。 MAPI では、3 つの行のデータが用意されています: MAPI のサブシステムに対応する行、行、MAPI スプーラーを無効、および統合アドレス帳の行です。 トランスポート プロバイダーは、状態テーブルに状態情報を提供する必要が、ため、すべてのアクティブなトランスポート プロバイダーの 1 つの行があります。 アドレス帳、メッセージ ストア プロバイダーは、状態テーブルをサポートするかどうかを選択できます。 
  
それぞれの行は、別のリソースによって提供されるがため、列のセットは行ごとにそれぞれ異なります。 ステータスのすべてのオブジェクトが指定する必要がある列のセット、MAPI が提供する列のセットがありません。 サービス プロバイダーは、プロバイダー固有のプロパティを公開するためのこれらのセットに追加できます。 たとえば、メッセージ ストア プロバイダーは、 **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) が、メッセージ ・ ストアの id をクライアントに提供するのにを追加できます。 クライアントが使用できる余分な情報の有無の事前知識が必要です。 
  
状態テーブルのすべての行にする必要があるプロパティを次の表に一覧します。 ステータス オブジェクトの実装は、いくつかのプロパティの他のユーザーは、MAPI によって計算されます。
  
|**ステータス オブジェクトによって提供されるプロパティ**|**MAPI によって提供されるプロパティ**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))、 **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) と**PR_IDENTITY_SEARCH_KEY** ([に設定する必要があります状態オブジェクトは、id を提供する場合PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))、これらのプロパティをテーブルに含めるとします。 
  
4 つのプロパティは、MAPI によってステータス テーブルの行ごとに計算されます。
  
|||
|:-----|:-----|
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI は、クライアントを開くには、対応する状態オブジェクトを有効にするのには [状態] 行に、エントリ id を割り当てます。 行識別子は、状態オブジェクト内のデータを識別するのには、インスタンスのキーが格納されるテーブルの行を識別するのにも割り当てられます。 MAPI_STATUS に**PR_OBJECT_TYPE**プロパティが設定されています。 
  
ステータス テーブルにアクセスするには、クライアントは、 [IMAPISession::GetStatusTable](imapisession-getstatustable.md)メソッドを呼び出します。 この呼び出しは、起動時にすぐにない実行する必要があります。 **GetStatusTable**には、トランスポート プロバイダーを初期化するために MAPI スプーラーが、クライアントが、ログオンを完了した後まで延期されている操作を待機するためです。 **GetStatusTable**は、MAPI スプーラーが起動処理を完了した後、比較的高速な呼び出しです。 
  
テーブルのステータス情報は、状態オブジェクトは、クライアントが接続されているまたはオフライン モードで実行されているかどうかを判断し、プロバイダーの状態を監視するためにアクセスするなど、さまざまな方法で使用できます。 などのクライアントは、 **PR_ENTRYID**プロパティの値を[IMAPISession::OpenEntry](imapisession-openentry.md)メソッドに渡すことによって、特定のサービス プロバイダーの状態のオブジェクトを開くことができます。 状態オブジェクトには、 **IMAPIStatus**インターフェイス、サービス プロバイダーのパスワードを変更する、メッセージ キューのフラッシュ、[設定] プロパティ シートを表示またはプロバイダーの状態を直接確認するメソッドを持つインターフェイスがサポートされています。 テーブルのステータス情報は、時間のかかる操作中に進行状況をクライアントに通知するダイアログ ボックスをビルドするのにも使用できます。 
  
状態テーブルをサポートしているサービス プロバイダーを作成し、その行を更新する[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを使用します。 その行に変更が発生すると、状態テーブルの通知を受信する登録されているシンク オブジェクトに通知する必要がありますすべてを案内します。 MAPI 通知ユーティリティを使用している各アドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを直接呼び出す場合、サービス プロバイダーは、 [IMAPISupport::Notify](imapisupport-notify.md)メソッドを呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

