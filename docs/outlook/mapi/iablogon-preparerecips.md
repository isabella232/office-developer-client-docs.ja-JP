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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423861"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング システムで後で使用する受信者リストを準備します。
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> [in]返される文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - MAPI_CACHE_ONLY: 名前解決を実行するには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
_lpPropTagArray_
  
> [in]更新が必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター (該当する場合)。 _lpPropTagArray パラメーター_ には NULL を指定できます。 
    
_lpRecipList_
  
> [in]受信者リストを [保持する ADRLIST](adrlist.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者リストが正常に準備されました。
    
MAPI_E_NOT_FOUND 
  
> _lpRecipList_ パラメーター内の 1 つ以上の受信者が存在しません。 
    
## <a name="return-value"></a>戻り値

クライアントは、MAPI [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) メソッドを呼び出して、1 つ以上の受信者のプロパティのセットを変更または再配置します。 受信者は、送信メッセージの受信者リストの一部である場合と一部ではない場合があります。 MAPI は、アドレス帳プロバイダーの **IABLogon::P repareRecips メソッドにこの呼び出しを転送** します。 
  
**IABLogon::P repareRecips は** 、次の 4 つの主要なタスクを実行します。 
  
- _lpRecipList_ パラメーターが指すアドレス一覧のすべての受信者に、長期的なエントリ識別子が設定されます。 
    
- すべての受信者が  _、lpPropTagArray_ パラメーターが指すプロパティ値配列で指定されたプロパティを持つ必要があります。 
    
- プロパティ値配列のプロパティが、呼び出し前に存在していた他のプロパティの前に表示されます。
    
- **ADRLIST** 構造内の各受信者の [ADRENTRY](adrentry.md)構造のプロパティの順序がプロパティ値配列と同じことを確認します。 
    
**lpRecipList** パラメーターの _ADRENTRY_ 構造には、受信者ごとに **1 つの ADRENTRY** 構造が含まれる。 各 **ADRENTRY 構造体** には、受信者のプロパティを記述する [SPropValue](spropvalue.md) 構造体の配列が含まれています。 **IABLogon::P repareRecips** が返される場合、各受信者の **SPropValue** 構造体配列には _、lpPropTagArray_ のプロパティと受信者の他のプロパティが含まれます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IABLogon::P repareRecips** を実装するには、プロパティを特定の順序で設定し、プロパティ値を取得し、短期エントリ識別子を長期エントリ識別子に変換します。 _lpPropTagArray_ パラメーターで要求されるプロパティは _、lpRecipList_ パラメーター内の各受信者の **ADRENTRY** 構造に関連付けられたプロパティ値配列の最初にある必要があります。 これらのプロパティの値が存在しない場合は、そのエントリ識別子を使用して関連付けられたメッセージング ユーザーまたは配布リストを開き、不足しているプロパティ値を取得します。 
  
_lpRecipList_ **で渡される各 SPropValue** 構造体を個別に割り当て、構造体を個別に解放できます。 文字列プロパティのデータを格納する **場合など、SPropValue** 構造体に追加の領域を割り当てる必要がある場合は [、MAPIAllocateBuffer](mapiallocatebuffer.md) 関数を使用して、完全なプロパティ値配列に追加の領域を割り当てる必要があります。 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して元のプロパティ値配列を解放し[、MAPIAllocateMore](mapiallocatemore.md)関数を使用して、必要な追加のメモリを割り当てる。 
  
**IABLogon::P repareRecips** を実装するには、次の手順を使用します。
  
1. _lpPropTagArray パラメーターのエントリを確認_ します。 プロパティ値の配列が空の場合、実行する作業はありません。 成功の値を返します。 
    
2. _lpRecipList パラメーターで各受信者を処理_ します。 リストには、 **受信者ごとに 1 つの ADRENTRY** 構造メンバーがあります。 次の種類の受信者を無視します。 
    
   - **ADRENTRY** 構造体の **rgPropVals** メンバーにエントリ識別子がない受信者 (つまり、未解決の受信者)。 
    
   - プロバイダーに属していないエントリ識別子を持つ受信者。 これらの受信者は、別のアドレス帳プロバイダーに渡されます。
    
3. 受信者を開き、受信者に対して既に設定されているプロパティを取得します。
    
4. _lpRecipList_ で指定されたプロパティ値の配列と **、GetProps** から返されるプロパティの配列を結合します。 両方のプロパティ配列で同じプロパティが発生する場合は  _、lpRecipList の値を使用します_。
    
5. _lpRecipList_ プロパティの値配列が必要なすべてのプロパティを保持するのに十分な大きい場合は、結合された配列に置き換える必要があります。 _lpRecipList プロパティ_ 値配列のサイズが十分ではない場合は、新しく割り当てられた配列に置き換える必要があります。 新しい配列の各 cValues メンバーに更新された値 **が設定されている必要** があります。 
    
6. _lpPropTagArray_ パラメーター内の 1 つ以上のプロパティが認識されない場合は、受信者の **ADRENTRY** 構造体のプロパティの種類を PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND または別の値に設定します。 プロパティの詳細についてはPT_ERRORプロパティの [種類を参照してください](property-types.md)。
    
> [!NOTE]
> **IABLogon::P repareRecips** に渡される **ADRLIST** 構造体を再割り当てしたり、エントリの数を変更したりしない。 
  
## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

