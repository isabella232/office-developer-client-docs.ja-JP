---
title: State プロパティ (ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479469"
---
# <a name="state-property-ado"></a>State プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。

非同期メソッドを実行する対象になるすべてのオブジェクトについて、オブジェクトの状態が接続、実行、取得のいずれであるかを示します。

## <a name="return-value"></a>戻り値

**ObjectStateEnum** の値になる長整数型 ( [Long](objectstateenum.md) ) の値を返します。既定値は **adStateClosed** です。

## <a name="remarks"></a>解説

**State** プロパティを使用して、特定のオブジェクトの現在の状態をいつでも調べることができます。

オブジェクトの **State** プロパティは、値の組み合わせになる場合があります。たとえば、ステートメントが実行中である場合、このプロパティの値は **adStateOpen** と **adStateExecuting** の組み合わせになります。

**State** プロパティは値の取得のみ可能です。

