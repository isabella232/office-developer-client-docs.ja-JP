---
title: DATE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: システムの地域設定の短い形式の日付形式に従って、年、月、および日によって表される日付が書式設定を返します。 年、月、および日の値は、グレゴリオ暦のカレンダーを反映します。
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805189"
---
# <a name="date-function-visioshapesheet"></a>DATE 関数 (VisioShapeSheet)

システムの地域設定の短い形式の日付形式に従って、*年、月*、*日*によって表される日付が書式設定を返します。 *年**月*、および*日*の値は、グレゴリオ暦のカレンダーを反映します。 
  
## <a name="syntax"></a>構文

日 (* **年** *、* **月** *、* **日** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |必須  <br/> |**Integer** <br/> |年を指定します。  <br/> |
| _month_ <br/> |必須  <br/> |**Integer** <br/> |月を指定します。  <br/> |
| _day_ <br/> |必須  <br/> |**Integer** <br/> |日を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

DATE(1999,6,7)
  
07.06.99 を表す値を返します。
  
## <a name="example-2"></a>例 2

DATE(1999,6,7) + 4 ed.
  
6/11/1999 を表す値を返します。
  
## <a name="example-3"></a>例 3

FORMAT(DATE(1999,10,14),"C")
  
1999 年 10 月 14 日、火曜日を表す値を返します。
  

