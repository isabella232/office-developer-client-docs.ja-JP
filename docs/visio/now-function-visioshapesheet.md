---
title: NOW 関数 (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
ms.localizationpriority: medium
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: 現在の日付と時刻の値を返します。
ms.openlocfilehash: 6ec4069334a4a11588d015b6b134926c75613188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627864"
---
# <a name="now-function-visioshapesheet"></a>NOW 関数 (VisioShapeSheet)

現在の日付と時刻の値を返します。
  
## <a name="syntax"></a>構文

NOW ( )
  
### <a name="return-value"></a>戻り値

Datetime
  
## <a name="remarks"></a>注釈

NOW は 1 分ごとに自動的に再計算されます。 
  
## <a name="example-1"></a>例 1

NOW( )
  
現在の日付と時刻 (9/27/2010 12:03:30 PM など) を返します。
  
## <a name="example-2"></a>例 2

FORMAT(NOW(),"dd MMM., yyyy hh:mm")
  
現在の日付と時刻を 27 Sep., 2010 12:03 のように書式設定して返します。
  
## <a name="example-3"></a>例 3

NOW()+2EW。
  
現在の日付と時刻から 2 週間経過した日付と時刻 (10/11/10 12:03:30 PM など) を返します。
  

