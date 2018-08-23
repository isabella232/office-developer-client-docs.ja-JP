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
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567014"
---
# <a name="attdate-attributes"></a>attDate の属性

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。 これら**DTR**の構造体としてすべてエンコードします。 日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。 
  
日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。 これら**DTR**の構造体としてすべてエンコードします。 日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。 
  
**DTR**構造体は、Win32 ヘッダー ファイルで定義されている**SYSTEMTIME**構造体に非常に似ています。 **DTR**の構造は、 **sizeof(DTR)** バイトの構造体の最初のメンバーで始まる、TNEF ストリームにエンコードされます。 **DTR**の構造は、TNEF で定義されます。H ヘッダー ファイルです。 
  

