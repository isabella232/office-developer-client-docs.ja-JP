---
title: Workspace.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ee787917a95e3716e629f87512caca1f408a6213
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617349"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close メソッド (DAO)


**適用先**: Access 2013、Office 2013

開いている **Workspace** を閉じます。

## <a name="syntax"></a>構文

*式* .Close

*expression*: **Workspace** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。

