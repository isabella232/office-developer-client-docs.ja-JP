---
title: 添付日付の属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318068"
---
# <a name="attdate-attributes"></a>添付日付の属性

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。 これらはすべて、 **DTR**構造体としてエンコードされます。 添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。 
  
日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。 これらはすべて、 **DTR**構造体としてエンコードされます。 添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。 
  
**DTR**構造体は、Win32 ヘッダーファイルで定義されている**SYSTEMTIME**構造に非常によく似ています。 **dtr**構造は、構造体の最初のメンバから始まる**sizeof (dtr)** バイトで、TNEF ストリームにエンコードされます。 **DTR**構造体は TNEF で定義されています。H ヘッダーファイル。 
  

