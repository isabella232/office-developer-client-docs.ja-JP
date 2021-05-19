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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415916"
---
# <a name="adrlist"></a>ADRLIST

**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上の受信者に属する 0 個以上のプロパティについて説明します。 
  
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

## <a name="members"></a>Members

**cEntries**
  
> **aEntries** メンバーで指定された配列内のエントリの数。 
    
**aEntries**
  
> [ADRENTRY 構造体の配列](adrentry.md)。受信者ごとに 1 つの構造。 
    
## <a name="remarks"></a>注釈

**ADRLIST 構造体には** 1 つ以上の **ADRENTRY** 構造が含まれています。それぞれが受信者のプロパティを記述します。 受信者は未解決にできます。 つまり、プロパティ値の配列にエントリ識別子が含まれます。 解決済み受信者は **、PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれるという意味です。 通常、解決済み受信者には、電子メール アドレス [(PidTagEmailAddress](pidtagemailaddress-canonical-property.md) **)** プロパティPR_EMAIL_ADDRESSアドレスが設定されています。 ただし、電子メール アドレスは必要ありません。 **ADRLIST 構造体** は、たとえば、送信メッセージの受信者リストを記述し、MAPI によってアドレス帳にエントリを表示するために使用されます。 
  
**ADRLIST 構造体** は [、テーブル内の行を](srowset.md) 表す場合に使用される SRowSet 構造体に似た構造です。 実際、これら 2 つの構造は、同じ意味で使用できるよう設計されています。 両方とも、プロパティのグループと配列内の値の数を記述する構造体の配列を含む。 **ADRLIST 構造体では、配列** には [ADRENTRY](adrentry.md)構造体が含まれていますが **、SRowSet** 構造体には [SRow 構造体が含](srow.md)まれています。 **ADRENTRY 構造** と **SRow 構造体** は、レイアウトで同じです。 **ADRLIST** 構造体と **SRowSet** 構造体は同じ割り当てルールに従うので、アドレス帳コンテナーの目次テーブルから取得される **SRowSet** 構造体を **ADRLIST** 構造にキャストし、この形式で使用できます。 
  
次の図は **、ADRLIST 構造のレイアウトを示** しています。 
  
**ADRLIST コンポーネント**
  
![ADRLIST コンポーネント](media/amapi_18.gif "ADRLIST コンポーネント")
  
**ADRLIST 構造体の ADRENTRY** 部分と [SPropValue](spropvalue.md)部分は、他の部分とは別に割り当て、解放する必要があります。 つまり **、ADRENTRY** 構造体のメモリが割り当てられた後 **、ADRENTRY** 構造体を解放する前に、各 SPropValue 構造体を個別に割り当てる必要があります。  このメモリ処理の独立性により、受信者と個々の受信者プロパティをアドレス一覧から自由に追加または削除できます。 
  
**ADRLIST** 構造体とそのすべての部分を割り当て、解放するには [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIFreeBuffer](mapifreebuffer.md)関数を使用する必要があります。 
  
受信者リストが大きすぎてメモリに収まらない場合、クライアントは [IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出して、リストのサブセットを処理できます。 この状況では、クライアントはアドレス帳の一般的なダイアログ ボックスを使用する必要があります。 
  
**ADRENTRY** 構造体にメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [MAPI の構造](mapi-structures.md)

