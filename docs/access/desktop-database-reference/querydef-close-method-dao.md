---
title: QueryDef.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 98fb593324cdae9c8164ca40f19834500a83acb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577032"
---
# <a name="querydefclose-method-dao"></a>QueryDef.Close メソッド (DAO)


**適用先:** Access 2013、Office 2013

開いている **QueryDef** を閉じます。

## <a name="syntax"></a>構文

*式* .Close

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Close** を使用したときに **QueryDef** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。

**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。

