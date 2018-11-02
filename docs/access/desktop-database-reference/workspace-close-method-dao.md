---
title: Workspace.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919851"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close メソッド (DAO)


**適用されます**Access 2013、Office 2013。

開いている **Workspace** を閉じます。

## <a name="syntax"></a>構文

*式*です。閉じる

*式***ワークスペース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。

