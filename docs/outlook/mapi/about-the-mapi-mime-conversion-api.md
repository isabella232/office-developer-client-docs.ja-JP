---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c36dd3e6761c5bb63fe6560bfa332d1b0548b689
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567929"
---
# <a name="about-the-mapi-mime-conversion-api"></a>MAPI-MIME 会話 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI-MIME 変換 API を使用すると、メール プロバイダーは MIME オブジェクトと MAPI メッセージの間で変換できます。 MAPI 定数に示すように、定数定義、クラス識別子、およびインターフェイス [識別子を提供します](mapi-constants.md)。 メール プロバイダーは **、CoCreateInstance** 関数を呼び出して **[IConverterSession](iconvertersessioniunknown.md)** のインスタンスを共同作成する必要があります。 
  

