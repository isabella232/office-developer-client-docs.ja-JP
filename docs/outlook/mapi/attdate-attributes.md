---
title: attDate の属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799710"
---
# <a name="attdate-attributes"></a>attDate の属性

  
  
**適用対象**: Outlook 
  
日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。 これら**DTR**の構造体としてすべてエンコードします。 日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。 
  
日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。 これら**DTR**の構造体としてすべてエンコードします。 日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。 
  
**DTR**構造体は、Win32 ヘッダー ファイルで定義されている**SYSTEMTIME**構造体に非常に似ています。 **DTR**の構造は、 **sizeof(DTR)** バイトの構造体の最初のメンバーで始まる、TNEF ストリームにエンコードされます。 **DTR**の構造は、TNEF で定義されます。H ヘッダー ファイルです。 
  

