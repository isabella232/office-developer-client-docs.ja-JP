---
title: 配布リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5fe588b31de1c84f1eba3633252cd265760fe378
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631075"
---
# <a name="creating-a-distribution-list"></a>配布リストの作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに配布リストを直接作成できます。
  
**PAB で配布リストを作成するには**
  
1. 次のように、1 つのプロパティ タグ [(PidTagDefCreateDl)](pidtagdefcreatedl-canonical-property.md)を **PR_DEF_CREATE_DLサイズの** プロパティ タグ配列を作成します。
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. [IAddrBook::GetPAB](iaddrbook-getpab.md)を呼び出して、PAB のエントリ識別子を取得します。 エラーが発生した場合、 **または GetPAB** がゼロまたは NULL を返す場合は、続行しない。 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. [IAddrBook::OpenEntry を呼び出して](iaddrbook-openentry.md)PAB を開きます。 _ulObjType 出力_ パラメーターは、次の値にMAPI_ABCONT。 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. PAB の [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_DEF_CREATE_DL プロパティ (配布リストの作成に使用するテンプレート) を取得します。 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. **GetProps が失敗** した場合: 
    
   1. PAB の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IMAPITable** インターフェイスで PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。  
      
   2. プロパティの制限を作成して、"MAPIPDL" PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列を使用して行を検索します。 
      
   3. [IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、この行を探します。 
    
6. **GetProps** または FindRow によって返されるエントリ識別子 **を保存します**。
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. PAB の [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、保存されたエントリ識別子で表されるテンプレートを使用して新しいエントリを作成します。 この呼び出しがリモートで行う場合、返されるオブジェクトがメッセージング ユーザーではなく配布リストになるとは想定されません。 エントリが 2 回CREATE_CHECK_DUPされるのを防ぐために  _、ulFlags_ パラメーターに CREATE_CHECK_DUP フラグが渡されます。 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. 新しいエントリの **IUnknown::QueryInterface** メソッドを呼び出し、IID_IDistList をインターフェイス識別子として渡して、エントリが配布リストであり [、IDistList : IMAPIContainer](idistlistimapicontainer.md) インターフェイスをサポートしているかどうかを判断します。 **CreateEntry は**、より具体的な **IMailUser** または **IDistList** ポインターではなく **IMAPIProp** ポインターを返すので、配布リスト オブジェクトが作成されたのを確認します。 **QueryInterface が** 成功した場合は、メッセージング ユーザーではなく配布リストを作成したと確認できます。 
    
9. 配布リストの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、表示名とその他のプロパティを設定します。 
    
10. 配布リストの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、1 つ以上のメッセージング ユーザーを追加します。 
    
11. 配布リストを保存する準備ができたら、配布リストの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。 保存された配布リストのエントリ識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定し、PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求する [IMAPIProp::GetProps](imapiprop-getprops.md) **を** 呼び出します。
    
12. **IUnknown::Release** メソッドを呼び出して、新しい配布リストと PAB を解放します。 
    
13. [MAPIFreeBuffer を呼](mapifreebuffer.md)び出して、PAB のエントリ識別子とサイズの大きなプロパティ タグ配列のメモリを解放します。 
    

