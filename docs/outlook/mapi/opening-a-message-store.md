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
  
プロファイルに応じて、クライアントは一般的なセッション中に1つ以上のメッセージストアを開く必要があります。 メッセージストアを開くことは、 [IMsgStore: imapiprop](imsgstoreimapiprop.md)実装へのポインターへのアクセスを得ることを意味します。 **IMsgStore**インターフェイスには、通知、フォルダー割り当ての作成、およびフォルダーとメッセージへのアクセスのためのメソッドが用意されています。 
  
クライアントは、ログオン時、およびプロファイルが変更されるときに、メッセージストアを開きます。 クライアントで、アクティブなセッション中にユーザーがプロファイルにメッセージストアを追加できるようにする場合は、それらをすぐに開くか、または次のセッションまで無視できます。 メッセージストアテーブルに通知を登録することによって、新しいメッセージストアの可用性に関する警告が表示されます。
  
メッセージストアを開くには、そのエントリ識別子を使用できるようにする必要があります。 ほとんどのクライアントは、メッセージストアテーブルを使用して開くメッセージストアのエントリ識別子にアクセスします。 ただし、メッセージストアによっては、エントリ識別子の形式が文書化されているため、クライアントがメッセージストアテーブルをバイパスし、必要なエントリ識別子を作成できるようになります。 このエントリ識別子を[imapisession:: openmsgstore](imapisession-openmsgstore.md)に直接渡すことができます。また、MAPI は、メッセージサービスに関連付けずにプロバイダーのプロファイルセクションを自動的に作成します。 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>メッセージストアテーブルからエントリ識別子を取得する
  
1. 呼び出し[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メッセージストアテーブルを開くことができます。 
    
2. **IMAPITable:: SetColumns**を呼び出して、テーブルを次の列を含む小さな列セットに制限します。 
    
   - **PR_PROVIDER_DISPLAY**または**PR_DISPLAY_NAME**
   - **PR_ENTRYID**プロパティ 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. 開くメッセージストアを表す行をフィルターで除外する制限を作成します。 既定のメッセージストアの検索の詳細については、「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。 名前でメッセージストアを検索するには、次のいずれかのプロパティ制限を適用します。
    
   - この種類のメッセージストアの一般的な名前を**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) と照合します。 たとえば、PR_PROVIDER_DISPLAY は "個人用フォルダー" に設定されている場合があります。
    
   - この種類のメッセージストアについて、 **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) を特定の**MAPIUID**に一致させます。 
    
   - この特定のメッセージストアの名前を**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と照合します。 たとえば、 **PR_DISPLAY_NAME**は "私のメッセージは会計年度 2010" に設定されている場合があります。 
    
4. [hrqueryallrows](hrqueryallrows.md)を呼び出して、メッセージストアテーブルから適切な行を取得します。 _pprows_パラメーターによって指定された行セットの arow **** member メンバーのプロパティ値配列に、その行のエントリ識別子が含まれます。 
    
5. [freeprows](freeprows.md)を呼び出して、 _pprows_が指す行セットを解放します。
    
6. **IUnknown:: release**メソッドを呼び出して、メッセージストアテーブルを解放します。 
    
メッセージストアを開くためのカスタムエントリ識別子を作成した場合は、 [WrapStoreEntryID](wrapstoreentryid.md)関数を呼び出して標準のエントリ識別子に変換します。 
  
メッセージストアのエントリ識別子を取得したら、次のいずれかのメソッドを呼び出して開きます。
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
メッセージストアにさまざまな特別なオプションを指定する必要がある場合は、 **openmsgstore**を呼び出します。 **openmsgstore**を使用すると、ダイアログボックスの表示を抑制したり、メッセージストアを一時的または非メッセージングストアとして指定したり、アクセスレベルを設定したり、エラーを遅延させたりすることができます。 **openentry**では、アクセスレベルを設定したり、エラーを遅延させることができます。 
  
MDB_NO_MAIL フラグを設定すると、メッセージストアがメッセージの送信または受信に使用されないことを MAPI に示します。 mapi は、このメッセージストアが存在することを mapi スプーラーに通知しません。 MDB_TEMPORARY フラグは、メッセージストアを一時的なものとして指定します。これは永続的な情報を格納するためには使用できません。 一時メッセージストアは、メッセージストアテーブルには表示されません。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

