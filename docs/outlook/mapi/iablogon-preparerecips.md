---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348945"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングシステムで後で使用するために、受信者リストを準備します。
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> 順番返される文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - MAPI_CACHE_ONLY: 名前解決を実行するのにオフラインアドレス帳のみを使用します。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
_lpPropTagArray_
  
> 順番更新が必要なプロパティがある場合は、そのプロパティを示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _lpPropTagArray_パラメーターは NULL にすることができます。 
    
_lpRecipList_
  
> 順番受信者の一覧を保持する[adrlist](adrlist.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者リストが正常に準備されました。
    
MAPI_E_NOT_FOUND 
  
> _lpRecipList_パラメーターの1人以上の受信者が存在しません。 
    
## <a name="return-value"></a>戻り値

クライアントは、MAPI [IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドを呼び出して、1人以上の受信者の一連のプロパティを変更または並べ替えます。 受信者は、送信メッセージの受信者の一覧に含まれていない場合もあれば、一部ではない場合もあります。 MAPI は、この呼び出しをアドレス帳プロバイダーの**IABLogon::P reparerecips**メソッドに転送します。 
  
**IABLogon::P reparerecips**は、次の4つの主要なタスクを実行します。 
  
- _lpRecipList_パラメーターによって指定されるアドレス一覧内のすべての受信者が長期間のエントリ識別子を持つようにします。 
    
- すべての受信者が、 _lpPropTagArray_パラメーターで指定されたプロパティ値配列で指定されたプロパティを持つことを確認します。 
    
- プロパティ値配列のプロパティが、呼び出し前に存在していた他のプロパティよりも前に表示されるようにします。
    
- **adrentry**構造内の各受信者の[adrentry](adrentry.md)構造のプロパティの順序が、プロパティの値の配列と同じになるようにします。 
    
_lpRecipList_パラメーターの**adrentry**構造には、各受信者の**adrentry**構造が1つ含まれています。 各**adrentry**構造には、受信者のプロパティを説明するための[spropvalue](spropvalue.md)構造の配列が含まれています。 **IABLogon::P reparerecips**が戻ると、各受信者の**spropvalue**構造体の配列には、 _lpPropTagArray_のプロパティと、受信者の他のプロパティが含まれます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

IABLogon の実装 **::P reparerecips**は、特定の順序にプロパティを配置し、プロパティの値を取得し、短時間のエントリ識別子を長期のエントリ識別子に変換します。 _lpPropTagArray_パラメーターで要求されるプロパティは、 _lpRecipList_パラメーターの各受信者の**adrentry**構造に関連付けられているプロパティ値の配列の先頭にある必要があります。 これらのプロパティの値が存在しない場合は、そのエントリ id を使用して、関連付けられているメッセージングユーザーまたは配布リストを開き、不足しているプロパティの値を取得します。 
  
_lpRecipList_で渡された各**spropvalue**構造を個別に割り当てて、構造体を個別に解放できるようにします。 文字列プロパティのデータを格納するなど、 **spropvalue**構造に追加の領域を割り当てる必要がある場合は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、完全なプロパティ値の配列に追加の領域を割り当てます。 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、元のプロパティの値の配列を解放した後、 [MAPIAllocateMore](mapiallocatemore.md)関数を使用して必要な追加のメモリを割り当てます。 
  
**IABLogon::P reparerecips**を実装するには、次の手順を使用します。
  
1. _lpPropTagArray_パラメーターのエントリを確認します。 プロパティの値の配列が空の場合、実行する作業はありません。 成功の値を返します。 
    
2. 各受信者を_lpRecipList_パラメーターで処理します。 リスト内の受信者ごとに1つの**adrentry**構造メンバーが存在します。 次の種類の受信者を無視します。 
    
   - **adrentry**構造の**rgPropVals**メンバにエントリ識別子を持たない受信者 (つまり、未解決の受信者)。 
    
   - プロバイダーに属さないエントリ識別子を持つ受信者。 これらの受信者は、別のアドレス帳プロバイダーに渡されます。
    
3. 受信者を開き、受信者に対して既に設定されているプロパティを取得します。
    
4. _lpRecipList_で指定されているプロパティ値の配列を、 **GetProps**から返されるプロパティの配列にマージします。 両方のプロパティ配列で同じプロパティが発生する場合は、 _lpRecipList_の値を使用します。
    
5. _lpRecipList_プロパティの値の配列が大きすぎて、必要なすべてのプロパティを保持できる場合は、結合された配列に置き換えます。 _lpRecipList_プロパティの値の配列が十分でない場合は、新たに割り当てられた配列に置き換えます。 新しい配列の各**cvalues**メンバーに、更新された値があることを確認してください。 
    
6. _lpPropTagArray_パラメーターで1つ以上のプロパティが認識されない場合は、受信者の**adrentry**構造のプロパティの種類を PT_ERROR に、プロパティ値を MAPI_E_NOT_FOUND またはその他の値に設定します。プロパティが利用できない特定の理由。 PT_ERROR の詳細については、「[プロパティの種類](property-types.md)」を参照してください。
    
> [!NOTE]
> IABLogon に渡される**adrlist**構造体を再割り当てせずに、 **reparerecips**またはエントリ数を変更することはありません。 
  
## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

