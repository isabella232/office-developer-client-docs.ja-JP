---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799559"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0020  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x00200102  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。
  
送信済みアイテムの既定のフォルダーは、**送信済みアイテム**です。
  
このプロパティは、POP3 および IMAP アカウントの読み取り専用です。 これらの種類のアカウントに対してこのプロパティを設定すると、 **E_ACCT_NOT_FOUND**が返されます。 
  

