---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9b2f73b6f70eea353a023a7285d210e508d6e6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551864"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者に属する 0 個以上のプロパティについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>メンバー

 **ulReserved1**
  
> 予約済み。は 0 である必要があります。
    
 **cValues**
  
> **rgPropVals** メンバーが指すプロパティ値配列内のプロパティの数。 **cValues メンバーには** 0 を指定できます。 
    
 **rgPropVals**
  
> 受信者のプロパティを記述するプロパティ値配列へのポインター。 **rgPropVals メンバー** には NULL を指定できます。 
    
## <a name="remarks"></a>注釈

**ADRENTRY 構造体は**、単一の受信者に属するプロパティを表します。 通常、受信者の説明に使用されるプロパティには、次のものが含まれます。 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
受信者の [SPropValue](spropvalue.md) **配列に** PR_ENTRYID識別子またはプロパティが表示される場合、これは受信者が解決済みかどうかを示します。 クライアントは [、IAddrBook::ResolveName](iaddrbook-resolvename.md) メソッドを呼び出して、送信メッセージの受信者リスト内のすべての受信者が解決済みである必要があります。 メッセージと一緒に送信できるのは、解決された受信者のみです。 
  
 **ADRENTRY** 構造体は、通常、ADRLIST 構造体 **の aEntries** メンバーの [配列を形成するために結合](adrlist.md) されます。 
  
 **ADRENTRY** 構造体と [SRow](srow.md) 構造体は、予約メンバー、プロパティ値の配列、および配列内の値の数を含むため、同じです。 **ADRENTRY** 構造体が結合され **、ADRLIST** 構造体の **aEntries** メンバーが形成されるのに対し **、SRow** 構造体は結合して [SRowSet](srowset.md)構造体の **aRow** メンバーを形成します。 どちらの構造も同じ割り当てルールに従います。これは、アドレス帳コンテナーの目次テーブルから取得された **SRowSet** 構造体を **ADRLIST** 構造にキャストし、この方法で使用できることを示しています。 
  
**ADRENTRY 構造体は** 空の場合があります。 たとえば **、IAddrBook::Address** の呼び出しで _lppAdrList_ パラメーターが指す **ADRLIST** 構造体に含まれる **ADRENTRY** 構造体は、受信者が削除されているときに空にできます。 
  
**ADRENTRY** 構造体にメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。
  
## <a name="see-also"></a>関連項目



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI の構造](mapi-structures.md)

