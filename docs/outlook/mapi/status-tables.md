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
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336464"
---
# <a name="status-tables"></a>状態テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態テーブルには、現在のセッションの状態に関する情報が含まれています。 mapi およびサービスプロバイダーによって提供される情報を含むすべての mapi セッションに対して、1つの状態テーブルがあります。 mapi では、mapi サブシステムの行、mapi スプーラーの行、統合アドレス帳の行という3つの行のデータが提供されます。 状態情報を状態テーブルに提供するにはトランスポートプロバイダーが必要であるため、アクティブなトランスポートプロバイダーごとに1つの行があります。 アドレス帳およびメッセージストアプロバイダーは、状態テーブルをサポートするかどうかを選択できます。 
  
各行は別のリソースによって提供されるため、列のセットは行ごとに異なる場合があります。 すべてのステータスオブジェクトに必要な列のセットと、MAPI が提供する列のセットがあります。 サービスプロバイダーは、これらのセットに追加して、プロバイダー固有のプロパティを公開することができます。 たとえば、メッセージストアプロバイダーが**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) を追加して、クライアントにメッセージストアの識別子を提供する場合があります。 クライアントは、この情報を使用できるようにするために、この特別な情報があるかどうかを事前に知っておく必要があります。 
  
次の表に、すべての状態テーブルの行に必要なプロパティを示します。 status オブジェクトの実装側は、いくつかのプロパティを提供します。他のユーザーは MAPI によって計算されます。
  
|**status オブジェクトによって提供されるプロパティ**|**MAPI で提供されるプロパティ**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
status オブジェクトが id を提供する場合は、 **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))、 **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))、および**PR_IDENTITY_SEARCH_KEY**を設定する必要があります ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) を指定し、これらのプロパティをテーブルに含めます。 
  
各状態テーブルの行では、次の4つのプロパティが MAPI によって計算されます。
  
|||
|:-----|:-----|
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI は、ステータス行にエントリ識別子を割り当てて、クライアントが対応する status オブジェクトを開くことができるようにします。 また、status オブジェクトのデータを識別するためのインスタンスキーとして、テーブル内の行を識別するための行識別子も割り当てられます。 **PR_OBJECT_TYPE**プロパティは MAPI_STATUS に設定されています。 
  
状態テーブルにアクセスするために、クライアントは[imapisession:: getstatustable](imapisession-getstatustable.md)メソッドを呼び出します。 この呼び出しは、スタートアップ時に直ちに行わないでください。 これは、 **getstatustable**が MAPI スプーラーによるトランスポートプロバイダーの初期化を待機する必要があるためです。これは、クライアントがログオンを終了するまで延期される操作です。 **getstatustable**は、MAPI スプーラーがスタートアップ処理を完了した後、比較的高速な呼び出しです。 
  
状態テーブル情報は、ステータスオブジェクトへのアクセスなど、さまざまな方法で使用でき、クライアントが接続モードまたはオフラインモードで実行されているかどうかを確認し、プロバイダーの状態を監視します。 たとえば、クライアントは、 **PR_ENTRYID**プロパティの値を[imapisession:: openentry](imapisession-openentry.md)メソッドに渡すことによって、特定のサービスプロバイダーの状態オブジェクトを開くことができます。 status オブジェクトは、 **imapistatus**インターフェイスをサポートしています。このインターフェイスには、サービスプロバイダのパスワードを変更するメソッド、メッセージキューをフラッシュするメソッド、構成プロパティシートを表示するメソッド、またはプロバイダーによる状態を直接確認するメソッドが含まれています。 状態テーブル情報を使用して、時間のかかる操作中にクライアントに進行状況を通知するダイアログボックスを作成することもできます。 
  
状態テーブルをサポートするサービスプロバイダーは、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを使用して、行を作成および更新します。 行が変更されるたびに、状態テーブル通知を受信するように登録されているすべてのアドバイズシンクオブジェクトに通知する必要があります。 MAPI 通知ユーティリティを使用している場合、または各アドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを直接呼び出している場合は、サービスプロバイダーは[imapisupport:: Notify](imapisupport-notify.md)メソッドを呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

