---
title: 配布リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424176"
---
# <a name="creating-a-distribution-list"></a>配布リストの作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに配布リストを直接作成することができます。
  
**PAB で配布リストを作成するには**
  
1. 次のように、 **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) という1つのプロパティタグを持つサイズ付きプロパティタグ配列を作成します。
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. [IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。 エラーが発生した場合、または**getpab**が0または NULL を返した場合は続行しません。 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、PAB を開きます。 _ulobjtype_出力パラメーターは、MAPI_ABCONT に設定する必要があります。 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. PAB の[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、配布リストを作成するために使用するテンプレートである PR_DEF_CREATE_DL プロパティを取得します。 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. **GetProps**が失敗した場合: 
    
   1. PAB の[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IMAPITable**インターフェイスを持つ**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。 
      
   2. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列が "mapipdl" に等しい行を検索するプロパティ制限を作成します。 
      
   3. この行を検索するには、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出します。 
    
6. **GetProps**または**FindRow**のどちらかによって返されるエントリ識別子を保存します。
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. PAB の[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、保存したエントリ id で表されるテンプレートを使用して新しいエントリを作成します。 この呼び出しがリモートである場合、返されるオブジェクトがメッセージングユーザーではなく配布リストであると仮定してはなりません。 CREATE_CHECK_DUP フラグは_ulflags_パラメーターで渡されるため、エントリが2回追加されることはありません。 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. 新しいエントリの**IUnknown:: QueryInterface**メソッドを呼び出して、IID_IDistList をインターフェイス識別子として渡し、エントリが配布リストであるかどうかを確認し、 [IMAPIContainer](idistlistimapicontainer.md)インターフェイスをサポートします。 **createentry**は、より具体的な**imailuser**または**imailuser**ポインターではなく**imapiprop**ポインターを返すので、配布リストオブジェクトが作成されたことを確認します。 **QueryInterface**が成功した場合は、メッセージングユーザーではなく、配布リストが作成されていることを確認できます。 
    
9. 配布リストの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、表示名とその他のプロパティを設定します。 
    
10. 配布リストの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、1つまたは複数のメッセージングユーザーを追加します。 
    
11. 保存する準備ができたら、配布リストの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 保存されている配布リストのエントリ識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定してから、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求する[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出します。
    
12. **IUnknown:: release**メソッドを呼び出して、新しい配布リストと PAB を解放します。 
    
13. [MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、PAB のエントリ識別子とサイズ付きプロパティタグ配列のメモリを解放します。 
    

