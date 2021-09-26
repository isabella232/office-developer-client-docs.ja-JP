---
title: 状態テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a3bb89cb54dafe6c3f82f4633c15ed4e67751448
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591067"
---
# <a name="status-tables"></a>状態テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態テーブルには、現在のセッションの状態に関連する情報が含まれている。 MAPI およびサービス プロバイダーによって提供される情報を含む MAPI セッションごとに 1 つの状態テーブルがあります。 MAPI は、MAPI サブシステムの行、MAPI スプーラーの行、および統合アドレス帳の行の 3 行のデータを提供します。 状態テーブルに状態情報を提供するにはトランスポート プロバイダーが必要なので、アクティブなトランスポート プロバイダーごとに 1 つの行があります。 アドレス帳とメッセージ ストア プロバイダーは、状態テーブルをサポートするかどうかを選択できます。 
  
各行は異なるリソースによって提供されるので、列のセットは行ごとに異なる場合があります。 すべての status オブジェクトが指定するために必要な列のセットと、MAPI が提供する列のセットがあります。 サービス プロバイダーは、これらのセットに追加して、プロバイダー固有のプロパティを公開できます。 たとえば、メッセージ ストア プロバイダーは、PR_STORE_RECORD_KEY[(PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)を追加して、クライアントにメッセージ ストアの識別子を提供します。  クライアントが使用するには、この追加情報の存在に関する事前の知識が必要です。 
  
次の表に、すべての状態テーブル行に含む必要があるプロパティを示します。 status オブジェクトの実装者は、プロパティの一部を提供します。その他は MAPI によって計算されます。
  
|**status オブジェクトによって提供されるプロパティ**|**MAPI によって提供されるプロパティ**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
status オブジェクトが ID を提供する場合 **は、PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay)](pidtagidentitydisplay-canonical-property.md) **、PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId)、](pidtagidentityentryid-canonical-property.md)および **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md)を設定し、これらのプロパティを表に含める必要があります。 
  
MAPI では、状態テーブル行ごとに 4 つのプロパティが計算されます。
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI は、クライアントが対応する状態オブジェクトを開くことができる状態行にエントリ識別子を割り当てる。 行識別子は、テーブル内の行を、状態オブジェクト内のデータを識別するためのインスタンス キーとして割り当てられます。 プロパティ **PR_OBJECT_TYPE** に設定MAPI_STATUS。 
  
状態テーブルにアクセスするには、クライアントは [IMAPISession::GetStatusTable メソッドを呼び出](imapisession-getstatustable.md) します。 この呼び出しは、起動時に直ちに行う必要があります。 **これは、GetStatusTable** が MAPI スプーラーがトランスポート プロバイダーを初期化するのを待つ必要があるためです。これは、クライアントがログオンを完了するまで延期される操作です。 **GetStatusTable** は、MAPI スプーラーがスタートアップ処理を完了した後の比較的高速な呼び出しです。 
  
状態テーブルの情報は、状態オブジェクトにアクセスしたり、クライアントが接続モードまたはオフライン モードで実行されているかどうかを判断したり、プロバイダーの状態を監視したりするために、さまざまな方法で使用できます。 たとえば、クライアントは **、PR_ENTRYID** プロパティの値を [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドに渡して、特定のサービス プロバイダーの状態オブジェクトを開きます。 status オブジェクトは **、IMAPIStatus** インターフェイスをサポートします。サービス プロバイダーのパスワードの変更、メッセージ キューのフラッシュ、構成プロパティ シートの表示、またはプロバイダーとの状態の直接確認を行うメソッドを含むインターフェイス。 状態テーブルの情報を使用して、長い操作中に進行状況をクライアントに通知するダイアログ ボックスを作成することもできます。 
  
状態テーブルをサポートするサービス プロバイダーは [、IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを使用して行を作成および更新します。 行に変更が発生するたびに、状態テーブル通知を受信するために登録されているすべてのアアドバイス シンク オブジェクトに通知する必要があります。 サービス プロバイダーは、MAPI 通知ユーティリティを使用している場合は [IMAPISupport::Notify](imapisupport-notify.md) メソッドを呼び出したり、各アドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドを直接呼び出したりできます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

