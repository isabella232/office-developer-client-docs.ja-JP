---
title: 受信者名の解決
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328673"
---
# <a name="resolving-a-recipient-name"></a>受信者名の解決

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージがアドレス指定されると、受信者リストは各受信者に関連するプロパティを使用して作成されます。 メッセージが送信されるときに、これらのプロパティの1つは、受信者の長い用語のエントリ id である必要があります。 各受信者に**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれていることを確認するには、受信者の一覧について説明する[adrlist](adrlist.md)構造を IAddrBook:: の呼び出しの_lpadrlist_パラメーターの内容に渡します。 [ResolveName](iaddrbook-resolvename.md)。
  
 **ResolveName**は、既に解決されている**adrlist**構造のエントリを無視することによって処理を開始します。これは、対応する[adrlist](adrentry.md)構造の**spropvalue**にエントリ識別子が存在することによって示されます。配列. 次に、 **ResolveName**は、1回限りのエントリ識別子を2種類の受信者に自動的に割り当てます。 
  
- アドレスがインターネットアドレスとして書式設定された受信者
    
- アドレスが次の形式に設定されている受信者。
    
     `displayname[address type:email address]`
    
残りのすべてのエントリについて、 **ResolveName**は、表示名の完全一致のアドレス帳を検索します。 **ResolveName**は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、検索するコンテナーのセットと検索順序を決定します。 MAPI は、すべてのコンテナーの[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出して、すべての名前の解決を試みます。 一部のコンテナーは**ResolveNames**をサポートしていないため、コンテナーが MAPI_E_NO_SUPPORT を返す場合、MAPI は、そのコンテンツテーブルに対して**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を適用します。 この制限を使用して名前解決をサポートするには、すべてのアドレス帳コンテナーが必要です。 すべての名前が解決されると、それ以降のコンテナー呼び出しは行われません。 すべてのコンテナーが呼び出されたが、あいまいまたは未解決の名前が残っている場合は、ユーザーに残りの名前の解決を求めるメッセージが表示される場合は、MAPI がダイアログボックスを表示します。
  
**PR_ANR**制限は、 **adrlist**構造の表示名に対する**PR_ANR**プロパティの値と一致します。 **PR_ANR**プロパティ制限を使用してコンテナーの contents テーブルの表示を制限すると、アドレス帳プロバイダーは、プロバイダーにとって意味のあるプロパティに一致する検索の種類として "最適な推測" を実行することになります。 たとえば、1つのアドレス帳プロバイダーは、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に対して受信者リスト内の名前と一致する場合がありますが、管理者はこのプロパティを選択できます。
  
 **アドレス帳コンテナーの contents テーブルに PR_ANR プロパティ制限を設定するには**
  
1. 次のコードに示すように、 [srestriction](srestriction.md)構造を作成します。 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. コンテンツテーブルの[IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出し、 **srestriction**構造を_lpRestriction_パラメーターとして渡します。 
    

