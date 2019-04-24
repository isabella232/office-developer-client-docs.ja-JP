---
title: Workspace メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305958"
---
# <a name="workspaceclose-method-dao"></a>Workspace メソッド (DAO)


**適用先:** Access 2013、Office 2013

開いている **Workspace** を閉じます。

## <a name="syntax"></a>構文

*式*。いったん

*式***Workspace**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。

