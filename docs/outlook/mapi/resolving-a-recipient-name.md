---
title: 受信者名を解決します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803761"
---
# <a name="resolving-a-recipient-name"></a>受信者名を解決します。

  
  
**適用されます**: Outlook 
  
メッセージが処理されると、ときに、各受信者に関連するプロパティを持つ受信者のリストが組み込まれています。 メッセージが送信されるまでに、長期のエントリ id を受信者のこれらのプロパティのいずれかの必要があります。 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが各受信者に含まれていることを確認するには、受信者リストは、 [IAddrBook への呼び出し内のパラメーターに_lpAdrList_の内容を記述する[ADRLIST](adrlist.md)構造体を渡します。ResolveName](iaddrbook-resolvename.md)。
  
 **ResolveName** **SPropValue**の対応する[ADRENTRY](adrentry.md)構造体の内のエントリの識別子が存在することが示されているように、既に解決された**ADRLIST**構造体のエントリを無視することで処理を開始します。配列です。 次に、 **ResolveName**は、2 種類の受信者に 1 回限りのエントリ id を自動的に割り当てます。 
  
- インターネット アドレスとして書式設定されたアドレスを持つ受信者
    
- 受信者アドレスの形式次のとおりです。
    
     `displayname[address type:email address]`
    
残りのすべてのエントリの**ResolveName**の表示名に正確に一致するアドレス帳が検索されます。 **ResolveName**では、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、一連のコンテナーを検索し、検索順序を決定します。 MAPI は、すべての名前を解決しようとするすべてのコンテナーの[IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。 コンテナーによってはサポートしていないため**ResolveNames**コンテナーには、MAPI_E_NO_SUPPORT が返された場合、MAPI には、その内容のテーブルに対して**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限が適用されます。 すべてのアドレス帳コンテナーは、この制限を名前解決をサポートする必要があります。 すべての名前が解決した後はそれ以上のコンテナーの呼び出しが行われます。 すべてのコンテナーが呼び出されると、あいまいな、または未解決の名前が残る場合は、MAPI では、残りの名前を解決するのにはユーザーに確認するの可能な場合にダイアログ ボックスが表示されます。
  
**PR_ANR**制限では、 **ADRLIST**構造体での表示名に対して**PR_ANR**プロパティの値と一致します。 **PR_ANR**プロパティの制限を持つコンテナーの内容のテーブルのビューを制限すると、「最適な推測」プロバイダーの意味のあるプロパティと一致する、検索の種類を実行するアドレス帳プロバイダーが発生します。 などの 1 つのアドレス帳プロバイダー可能性があります常に名と一致**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に対しては、受信者の一覧でプロパティを選択するには管理者は、別可能性があります。
  
 **アドレス帳コンテナーの内容のテーブルで PR_ANR プロパティの制限を設定するのには**
  
1. 次のコードに示すように[SRestriction](srestriction.md)構造体を作成します。 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. 内容**SRestriction**構造体を_lpRestriction_パラメーターとして渡して、テーブルの[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出します。 
    

