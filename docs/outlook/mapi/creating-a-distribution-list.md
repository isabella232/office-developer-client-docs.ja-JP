---
title: 配布リストを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 82fa28f021dbb839c7bb05974682f0bb24174bb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799852"
---
# <a name="creating-a-distribution-list"></a>配布リストを作成します。

**適用対象**: Outlook 
  
クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに直接配布リストを作成することができます。
  
**個人アドレス帳の配布リストを作成するには**
  
1. プロパティを 1 つのタグ、 **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) で次のようにサイズのプロパティ タグ配列を作成します。
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. 個人アドレス帳のエントリ id を取得するために[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。 エラーが発生、または**GetPAB**には、0 または NULL が返されますが続行されません。 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. 開くには、個人用アドレス帳[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 _UlObjType_の出力パラメーターは、MAPI_ABCONT に設定する必要があります。 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. PR_DEF_CREATE_DL プロパティを使用して、配布リストを作成するテンプレートを取得するために、個人用アドレス帳の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. **GetProps**が失敗した場合。 
    
   1. **IMAPITable**インターフェイスを使用して**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くには、個人用アドレス帳の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
      
   2. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) の列が"MAPIPDL"にします行を検索するプロパティ条件を作成します。 
      
   3. この行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 
    
6. **GetProps**または**FindRow**のいずれかによって返されるエントリの識別子を保存します。
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. 保存されたエントリの識別子によって表されたテンプレートを使用して新しいエントリを作成するのには、個人用アドレス帳の[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドを呼び出します。 返されるオブジェクトされるメッセージングのユーザーではなく、配布リストと、この呼び出しはリモートとは限りません。 _UlFlags_パラメーター エントリが 2 回追加されることを防ぐために CREATE_CHECK_DUP フラグが渡されることに注意してください。 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. IID_IDistList を渡すことを確認エントリ、配布リストをサポートするのには、インターフェイス識別子と、新しいエントリの**IUnknown::QueryInterface**メソッドを呼び出して、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースです。 **CreateEntry**は、特定の**IMailUser**または**IDistList**のポインターではなく、 **IMAPIProp**ポインターを返す、ために、配布リスト オブジェクトが作成されたことを確認します。 **QueryInterface**が成功した場合、メッセージングのユーザーではなく、配布リストが作成されていることを確認できます。 
    
9. 表示名およびその他のプロパティを設定するのには、配布リストの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 
    
10. 1 つまたは複数のメッセージングのユーザーを追加するのには、配布リストの[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドを呼び出します。 
    
11. 保存する準備ができたら、配布リストの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 保存されている配布リストのエントリの識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定し、 [IMAPIProp::GetProps](imapiprop-getprops.md) ([PidTagEntryId](pidtagentryid-canonical-property.md)) の**PR_ENTRYID**プロパティを要求するを呼び出します。
    
12. **** メソッドを呼び出すことによって新しい配布リストと、個人用アドレス帳を解放します。 
    
13. 個人用アドレス帳およびサイズのプロパティ タグ配列のエントリの識別子のメモリを解放するのには[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。 
    

