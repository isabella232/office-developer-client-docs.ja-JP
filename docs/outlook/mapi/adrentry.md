---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421439"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者に属する0個以上のプロパティを記述します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> 予約語0である必要があります。
    
 **cvalues**
  
> **rgPropVals**メンバーによって参照されているプロパティ値配列のプロパティの数。 **cvalues**メンバーは0にすることができます。 
    
 **rgPropVals**
  
> 受信者のプロパティを説明するプロパティ値配列へのポインター。 **rgPropVals**メンバーは NULL にすることができます。 
    
## <a name="remarks"></a>注釈

**adrentry**構造は、1人の受信者に属するプロパティを示します。 通常、受信者を表すために使用されるプロパティには、次のようなものがあります。 
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
  
受信者の[spropvalue](spropvalue.md)配列にエントリ識別子または**PR_ENTRYID**プロパティが表示される場合、これは受信者が解決されたことを示します。 クライアントは[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドを呼び出して、送信メッセージの受信者一覧内のすべての受信者が解決されたことを確認します。 解決された受信者のみがメッセージと共に送信できます。 
  
 通常、 **adrentry**構造体は、 [adrentry](adrlist.md)構造体の**aentries**メンバーの配列を形成するために組み合わされています。 
  
 **adrentry**構造体と[srow](srow.md)構造体の両方には、予約済みのメンバー、プロパティ値の配列、および配列内の値の数が含まれているため、同一です。 **adrentry**構造体は**adrentry**構造体の**aentries**メンバーを形成するために組み合わされていますが、 **srow**構造体は、 [srow](srowset.md)構造の**arow**メンバーを形成するために組み合わされています。 両方の種類の構造体は同じ割り当てルールに従い、アドレス帳コンテナーの contents テーブルから取得された**srowset**構造を**adrlist**構造体にキャストして、そのものとして使用できるということを意味します。 
  
**adrentry**構造は空にすることができます。 たとえば、lppadrlist パラメーターによって指定さ**** れた adrentry 構造が、 **IAddrBook::** の呼び出しで**** _lppadrlist_パラメーターによって指定されている場合は、受信者が削除されているときに空になることがあります。 
  
**adrentry**構造にメモリを割り当てる方法の詳細については、「 [adrentry および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI の構造](mapi-structures.md)

