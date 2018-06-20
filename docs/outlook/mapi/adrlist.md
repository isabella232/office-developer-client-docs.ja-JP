---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b2d3dce7835f92d9ad78f7d8837e655fdd8fd412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799657"
---
# <a name="adrlist"></a>ADRLIST

**適用されます**: Outlook 
  
1 つまたは複数の受信者に所属する 0 個以上のプロパティについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbADRLIST](cbadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>メンバー

**cEntries**
  
> **AEntries**メンバーによって指定された配列内のエントリの数です。 
    
**aEntries**
  
> [ADRENTRY](adrentry.md)構造体の配列、各受信者の 1 つの構造体です。 
    
## <a name="remarks"></a>備考

**ADRLIST**構造体は、各受信者のプロパティを記述する 1 つまたは複数の**ADRENTRY**構造体を格納します。 受信者が解決することができます。 これは、プロパティ値の配列内のエントリ識別子を欠けていることを意味します。 受信者が解決されたことを意味します**PR\_エントリ ID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが含まれます。 通常、受信者の解決は、電子メール アドレス ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) である**PR_EMAIL_ADDRESS**プロパティもあります。 ただし、電子メール アドレスは必要ではありません。 **ADRLIST**構造体は、たとえば、MAPI アドレス帳にエントリを表示するのには、送信メッセージの受信者の一覧を記述する使用されます。 
  
[SRowSet](srowset.md)構造体のテーブル内の行を表すために使用する構造体**ADRLIST**の構造と似ています。 実際には、これら 2 つの構造体は、同じ意味で使用できるように設計されています。 両方には、プロパティのグループと、配列内の値の数を記述する構造体の配列が含まれています。 **ADRLIST**構造体の配列が含まれますが、 **SRowSet**構造体、配列内の[ADRENTRY](adrentry.md)の構造体には、 [SRow](srow.md)構造体が含まれています。 **ADRENTRY**構造体および**SRow**の構造体は、レイアウトでは同じです。 **ADRLIST**と**SRowSet**構造体は、同じ割り当て規則に従う、ため、アドレス帳コンテナーのコンテンツ テーブルから取得した**SRowSet**構造体は**ADRLIST**構造体へのキャストし、そのまま使用します。 
  
次の図は、 **ADRLIST**構造体のレイアウトを示しています。 
  
**ADRLIST コンポーネント**
  
![ADRLIST コンポーネント](media/amapi_18.gif "ADRLIST コンポーネント")
  
**ADRLIST**構造体の**ADRENTRY**と[SPropValue](spropvalue.md)の部分を割り当てられ、他の部分とは別に解放する必要があります。 つまり、各**SPropValue**構造体割り当てる必要があります個別に**ADRENTRY**構造体のメモリが割り当てられ、 **ADRENTRY**構造体が解放される前に解放された後。 メモリを処理するときのこの独立性は、自由に追加または、[アドレス] ボックスの一覧から削除するには、受信者と受信者のプロパティを個別に使用できます。 
  
割り当ておよび**ADRLIST**の構造とそのすべての部分を解放する[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIFreeBuffer](mapifreebuffer.md)関数を使用する必要があります。 
  
受信者の一覧がメモリに収まるように大きすぎる場合は、クライアントは、リストのサブセットを処理する[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことができます。 クライアントでは、アドレス帳コモン ダイアログ ボックスでこのような場合は使用しないでください。 
  
**ADRENTRY**構造体にメモリを割り当てる方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [MAPI の構造](mapi-structures.md)

