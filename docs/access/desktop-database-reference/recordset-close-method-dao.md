---
title: Recordset.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2cde1f91affb1a50d050feaa1fb5d637ab2e9b43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597031"
---
# <a name="recordsetclose-method-dao"></a>Recordset.Close メソッド (DAO)


**適用先**: Access 2013、Office 2013

開いている **Recordset** を閉じます。

## <a name="syntax"></a>構文

*式* .Close

*式* **Recordset** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。

**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。

