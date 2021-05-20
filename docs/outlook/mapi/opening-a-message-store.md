---
title: メッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432374"
---
# <a name="opening-a-message-store"></a>メッセージ ストアを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルによっては、クライアントは一般的なセッション中に 1 つ以上のメッセージ ストアを開く必要があります。 メッセージ ストアを開くとは、 [その IMsgStore : IMAPIProp](imsgstoreimapiprop.md) 実装へのポインターへのアクセスを得るという意味です。 **IMsgStore インターフェイスには**、通知、フォルダーの割り当て、フォルダーとメッセージへのアクセスのためのメソッドが提供されます。 
  
クライアントは、ログオン時とプロファイルの変更時にメッセージ ストアを開きます。 クライアントがアクティブ セッション中にユーザーがプロファイルにメッセージ ストアを追加することを許可している場合は、すぐに開くか、次のセッションまで無視できます。 メッセージ ストア テーブルに通知を登録すると、新しいメッセージ ストアの可用性が通知されます。
  
メッセージ ストアを開くには、そのエントリ識別子を使用できる必要があります。 ほとんどのクライアントは、メッセージ ストア テーブルから開くメッセージ ストアのエントリ識別子にアクセスします。 ただし、一部のメッセージ ストアでは、エントリ識別子の形式を文書化するため、クライアントはメッセージ ストア テーブルをバイパスして、必要なエントリ識別子を構築できます。 このエントリ識別子を [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) に直接渡し、MAPI はメッセージ サービスに関連付けずにプロバイダーのプロファイル セクションを自動的に作成します。 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>メッセージ ストア テーブルからエントリ識別子を取得する
  
1. [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出して、メッセージ ストア テーブルを開きます。 
    
2. **IMAPITable::SetColumns** を呼び出して、テーブルを次の列を含む小さな列セットに制限します。 
    
   - **PR_PROVIDER_DISPLAY** または **PR_DISPLAY_NAME**
   - **PR_ENTRYID** プロパティ 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. 開くメッセージ ストアを表す行をフィルター処理する制限を作成します。 既定のメッセージ ストアを探す方法の詳細については、「既定のメッセージ ストアを開 [く」を参照してください](opening-the-default-message-store.md)。 名前でメッセージ ストアを検索するには、次のプロパティ制限を適用します。
    
   - この **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)とこの種類のメッセージ ストアの一般的な名前を一致します。 たとえば、ユーザー PR_PROVIDER_DISPLAY "個人用フォルダー" に設定できます。
    
   - この **PR_MDB_PROVIDER** の **MAPIUID** と一致するメッセージ ストア ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) を指定します。 
    
   - この **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)とこの特定のメッセージ ストアの名前を一致します。 たとえば、PR_DISPLAY_NAME"2010 会計年度のマイ メッセージ" に設定できます。  
    
4. [HrQueryAllRows を呼び出](hrqueryallrows.md)して、メッセージ ストア テーブルから適切な行を取得します。 行のエントリ識別子は _、pprows_ パラメーターが指す行セットの **aRow** メンバーのプロパティ値配列に含まれます。 
    
5. [FreeProws を呼び出](freeprows.md)して、pprows が指す行セット _を解放します_。
    
6. メッセージ ストア テーブルを解放するには、 **その IUnknown::Release メソッドを呼び出** します。 
    
開くメッセージ ストアのカスタム エントリ識別子を作成した場合は [、WrapStoreEntryID](wrapstoreentryid.md) 関数を呼び出して、標準エントリ識別子に変換します。 
  
メッセージ ストアのエントリ識別子を取得した後、次のいずれかのメソッドを呼び出して開きます。
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
メッセージ ストアのさまざまな特別なオプションを指定する必要がある場合は **、OpenMsgStore** を呼び出します。 **OpenMsgStore** を使用すると、ダイアログ ボックスの表示を抑制し、メッセージ ストアを一時的なストアまたは非メッシュ ストアとして識別し、アクセス レベルを設定し、エラーを延期できます。 **OpenEntry では** 、アクセス レベルの設定とエラーの延期のみを行います。 
  
メッセージ のMDB_NO_MAIL設定すると、メッセージ ストアはメッセージの送受信に使用されません。 MAPI では、このメッセージ ストアの存在について MAPI スプーラーには通知されません。 このMDB_TEMPORARYは、メッセージ ストアを一時的なものとして指定します。これは、永続的な情報を格納するために使用できないことを示します。 一時メッセージ ストアは、メッセージ ストア テーブルには表示されません。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

