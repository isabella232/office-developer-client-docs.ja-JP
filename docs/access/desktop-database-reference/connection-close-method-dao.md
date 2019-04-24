---
title: Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295962"
---
# <a name="connectionclose-method-dao"></a>Close メソッド (DAO)


**適用先:** Access 2013、Office 2013

開いている **Connection** を閉じます。

## <a name="syntax"></a>構文

*式*。いったん

*式***Connection**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。

**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。

