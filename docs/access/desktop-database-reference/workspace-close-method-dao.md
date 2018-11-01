---
title: Workspace.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884129"
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

