---
title: DATE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
ms.localizationpriority: medium
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: システムの地域情報の短い日付スタイルに従って書式設定された年、月、および日で表される日付を設定。 年、月、および日の値は、グレゴリオ暦を反映します。
ms.openlocfilehash: 820329bbe9283cae540625d4232d4095c6a1a530
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577907"
---
# <a name="date-function-visioshapesheet"></a>DATE 関数 (VisioShapeSheet)

システムの地域情報の短い日付スタイルに従って書式設定された年、月、および日で表される日付を設定。 年、月 *、**および* 日の値 *は*、グレゴリオ暦を反映します。 
  
## <a name="syntax"></a>構文

DATE(** *year* **, ** *month* **, ** *day* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |年を指定します。  <br/> |
| _month_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |月を指定します。  <br/> |
| _day_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |日を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

DATE(1999,6,7)
  
07.06.99 を表す値を返します。
  
## <a name="example-2"></a>例 2

DATE(1999,6,7) + 4 ed.
  
6/11/1999 を表す値を返します。
  
## <a name="example-3"></a>例 3

FORMAT(DATE(1999,10,14),"C")
  
1999 年 10 月 14 日、火曜日を表す値を返します。
  

