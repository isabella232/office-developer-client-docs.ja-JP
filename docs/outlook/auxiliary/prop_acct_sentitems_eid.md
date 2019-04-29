---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431842"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0020  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x00200102  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。
  
送信済みアイテムの既定のフォルダーは、[**送信済みアイテム**] です。
  
このプロパティは、POP3 および IMAP のアカウントでは値の取得のみ可能です。 これらの種類のアカウントに対してこのプロパティを設定しようとすると、 **E_ACCT_NOT_FOUND**が返されます。 
  

