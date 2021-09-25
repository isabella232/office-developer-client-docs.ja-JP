---
title: attDate 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c4b58a5391565fd9a50ed0730cf53ed7e9b8af9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580273"
---
# <a name="attdate-attributes"></a>attDate 属性

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。 これらはすべて **DTR 構造としてエンコード** されます。 添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。 
  
日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。 これらはすべて **DTR 構造としてエンコード** されます。 添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。 
  
**DTR 構造は****、Win32** ヘッダー ファイルで定義されている SYSTEMTIME 構造と非常に似ています。 **DTR 構造体** は、構造体の最初のメンバーで始まる **sizeof(DTR)** バイトとして TNEF ストリームにエンコードされます。 **DTR 構造** は TNEF で定義されます。H ヘッダー ファイル。 
  

