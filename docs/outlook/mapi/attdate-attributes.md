---
title: attDate 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408279"
---
# <a name="attdate-attributes"></a>attDate 属性

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。 これらはすべて **DTR 構造としてエンコード** されます。 添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。 
  
日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。 これらはすべて **DTR 構造としてエンコード** されます。 添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。 
  
**DTR 構造は****、Win32** ヘッダー ファイルで定義されている SYSTEMTIME 構造と非常に似ています。 **DTR 構造体** は、構造体の最初のメンバーで始まる **sizeof(DTR)** バイトとして TNEF ストリームにエンコードされます。 **DTR 構造** は TNEF で定義されます。H ヘッダー ファイル。 
  

