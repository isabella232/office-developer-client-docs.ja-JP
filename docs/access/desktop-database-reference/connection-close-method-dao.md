---
title: Connection.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 120ad21231187aa2cba21e1ef55c6f9d135b6934
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590082"
---
# <a name="connectionclose-method-dao"></a>Connection.Close メソッド (DAO)


**適用先**: Access 2013、Office 2013

開いている **Connection** を閉じます。

## <a name="syntax"></a>構文

*式* .Close

*式***Connection** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。

**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。

