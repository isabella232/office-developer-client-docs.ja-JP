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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19799669"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**適用対象**: Outlook 
  
受信者に所属する 0 個以上のプロパティについて説明します。
  
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

## <a name="members"></a>Members

 **ulReserved1**
  
> 予約されています。0 にする必要があります。
    
 **あう**
  
> **RgPropVals**メンバーが指すプロパティの値の配列内のプロパティの数です。 **あう**メンバーは、0 にすることができます。 
    
 **rgPropVals**
  
> 受信者のプロパティを記述するプロパティ値の配列へのポインター。 **RgPropVals**のメンバーには、NULL を指定できます。 
    
## <a name="remarks"></a>注釈

**ADRENTRY**構造体では、1 人の受信者のプロパティについて説明します。 受信者の記述に使用される一般的なプロパティを以下に示します。 
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
  
エントリの識別子または**PR_ENTRYID**プロパティが表示されたら[SPropValue](spropvalue.md)配列の受信者に、受信者が解決されたことを示します。 クライアントは、送信メッセージの受信者の一覧のすべての受信者が解決されたことを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを呼び出します。 解決受信者のみにメッセージを送信できます。 
  
 **ADRENTRY**構造体は通常、 **aEntries** 、 [ADRLIST](adrlist.md)構造体のメンバーの配列を作成する結合します。 
  
 **ADRENTRY**構造体および[SRow](srow.md)の構造体は、両方を含むので、予約済みのメンバー プロパティの値の配列、配列内の値の数と同じです。 **ADRENTRY**構造体は、 **aEntries** 、 **ADRLIST**構造体のメンバーをフォームに組み合わせることで、一方、 **SRow**構造体は、 **aRow** 、 [SRowSet](srowset.md)構造体のメンバーをフォームに結合されます。 構造体の両方の種類は、アドレス帳コンテナーのコンテンツ テーブルから取得した**SRowSet**構造体の**ADRLIST**構造体へのキャストし、は、使用することを示す、同じ割り当て規則に従います。 
  
**ADRENTRY**構造体を空にすることができます。 たとえば、 **IAddrBook::Address**への呼び出し内の_lppAdrList_パラメーターで指定された**ADRLIST**構造体に含まれる**ADRENTRY**構造体は、受信者が削除されるときに空。 
  
**ADRENTRY**構造体にメモリを割り当てる方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI の構造](mapi-structures.md)

