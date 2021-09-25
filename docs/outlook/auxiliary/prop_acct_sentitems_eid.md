---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: アカウントの送信されたアイテムの既定のフォルダーのエントリ ID を表します。
ms.openlocfilehash: e9073a5b113ddd1181cb46ce44ac238833893636
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614347"
---
# <a name="prop_acct_sentitems_eid"></a>PROP_ACCT_SENTITEMS_EID

アカウントの送信されたアイテムの既定のフォルダーのエントリ ID を表します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0020  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x00200102  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。
  
送信されたアイテムの既定のフォルダーは [送信された **アイテム] です**。
  
このプロパティは、POP3 アカウントと IMAP アカウントの読み取り専用です。 これらの種類のアカウントに対してこのプロパティを設定しようとすると **、E_ACCT_NOT_FOUND。** 
  

