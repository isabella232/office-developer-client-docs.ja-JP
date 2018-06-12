---
title: NOW 関数 (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: 現在の日付と時刻の値を返します。
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805954"
---
# <a name="now-function-visioshapesheet"></a>NOW 関数 (VisioShapeSheet)

現在の日付と時刻の値を返します。
  
## <a name="syntax"></a>構文

NOW ( )
  
### <a name="return-value"></a>�߂�l

日付/時刻
  
## <a name="remarks"></a>注釈

NOW は 1 分ごとに自動的に再計算されます。 
  
## <a name="example-1"></a>例 1

NOW( )
  
現在の日付と時刻 (9/27/2010 12:03:30 PM など) を返します。
  
## <a name="example-2"></a>例 2

FORMAT(NOW(),"dd MMM., yyyy hh:mm")
  
現在の日付と時刻を 27 Sep., 2010 12:03 のように書式設定して返します。
  
## <a name="example-3"></a>例 3

NOW()+2EW.
  
現在の日付と時刻から 2 週間経過した日付と時刻 (10/11/10 12:03:30 PM など) を返します。
  

