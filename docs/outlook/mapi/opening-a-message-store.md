---
title: メッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 39d6df6db329abf7509f816165341ea0eda8331b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801672"
---
# <a name="opening-a-message-store"></a>メッセージ ストアを開く

**適用されます**: Outlook 
  
プロファイルによっては、クライアントは、通常のセッション中に 1 つまたは複数のメッセージ ストアを開く必要があります。 ポインターへのアクセスは、メッセージ ストアを開く、 [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)の実装です。 **IMsgStore**インターフェイスは、通知、フォルダーの割り当て、およびフォルダーやメッセージにアクセスするためのメソッドを提供します。 
  
クライアントは、プロファイルが変更されている場合、ログオン時のメッセージ ストアを開きます。 クライアントは、アクティブなセッション中に、メッセージ ・ ストアをプロファイルに追加するユーザーを許可している場合にすぐに開くか、次のセッションまでそれらを無視します。 メッセージ ストアのテーブル上の通知の登録、新しいメッセージ ストアの可用性に警告表示されます。
  
メッセージ ストアを開くには、エントリ id を使用する必要があります。 ほとんどのクライアントはアクセスを開くには、メッセージ ストアのテーブルを使用するメッセージ ・ ストアのエントリの識別子です。 ただし、いくつかのメッセージは、クライアントがメッセージ ストアのテーブルをバイパスし、必要なエントリの識別子を作成するようにして、そのエントリ id の形式のドキュメントを格納します。 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)に直接このエントリの識別子を渡すことができ、MAPI 自動的にプロファイル プロバイダーの作成、メッセージ サービスに関連付けることのないです。 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>メッセージ ストアのテーブルからエントリ識別子を取得します。
  
1. メッセージ ストアのテーブルを開くには、 [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出します。 
    
2. 次の列を含む列の小さなセットにテーブルを制限するのには**IMAPITable::SetColumns**を呼び出します。 
    
   - **PR_PROVIDER_DISPLAY**または**PR_DISPLAY_NAME**
   - **PR_ENTRYID**プロパティ 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. メッセージ ・ ストアを開くことを表す行を除外する制約を作成します。 既定のメッセージ ストアの検索に関する詳細については、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。 メッセージ ストアの名前で検索するには、プロパティの制限を次のいずれかを適用します。
    
   - メッセージ ・ ストアのこのタイプの一般名と**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) に一致します。 たとえば、「個人用フォルダー」に PR_PROVIDER_DISPLAY を設定する場合があります。
    
   - メッセージ ・ ストアのこのタイプの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) とは、特定の**MAPIUID**に一致します。 
    
   - この特定のメッセージ ストアの名前と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致します。 「マイ メッセージ 2010 の会計年度」に**PR_DISPLAY_NAME**を設定する可能性があります、 
    
4. メッセージ ストアのテーブルから適切な行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 行のエントリの識別子は、 _pprows_パラメーターで指定された行セットの**aRow**メンバーのプロパティ値の配列に含まれます。 
    
5. _Pprows_で指定された行セットを解放するために[FreeProws](freeprows.md)を呼び出します。
    
6. リリース、**リ ス**のメソッドを呼び出してメッセージ ストアのテーブルです。 
    
メッセージ ・ ストアを開くためのカスタムのエントリ id を作成した場合は、標準的なエントリの識別子に変換する[WrapStoreEntryID](wrapstoreentryid.md)関数を呼び出します。 
  
メッセージ ストアのエントリの識別子がある場合は後、を開くには、次の方法のいずれかを呼び出します。
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
**OpenMsgStore**は、さまざまなメッセージ ・ ストア用の特別なオプションを指定する必要がある場合に呼び出します。 **OpenMsgStore** ] ダイアログ ボックスの表示を抑制するには、一時的、または、アクセス レベルの設定、メッセージングのストアとしては、メッセージ ・ ストアを識別し、エラーを保留にできます。 **OpenEntry**では、アクセス レベルを設定し、エラーを遅らせることができます。 
  
MDB_NO_MAIL を設定するフラグを示します MAPI にない送信または受信メッセージのメッセージ ・ ストアを使用すること。 MAPI には、このメッセージ ・ ストアの存在についての MAPI スプーラー通知しません。 MDB_TEMPORARY フラグは、永続的な情報を格納する使用することはできませんという意味と、一時的なメッセージ ・ ストアを指定します。 一時的なメッセージ ・ ストアは、メッセージ ストアの表には表示されません。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

