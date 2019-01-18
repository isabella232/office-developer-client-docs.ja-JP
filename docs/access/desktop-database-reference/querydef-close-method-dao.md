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
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720003"
---
# <a name="querydefclose-method-dao"></a>QueryDef.Close メソッド (DAO)


**適用されます**Access 2013、Office 2013。

開いている **QueryDef** を閉じます。

## <a name="syntax"></a>構文

*式*です。閉じる

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** を使用したときに **QueryDef** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。

代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。

