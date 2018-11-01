---
title: Connection.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4cc4230c7d647d58c0f30bd8351118e6c44198a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879698"
---
# <a name="connectionclose-method-dao"></a>Connection.Close メソッド (DAO)


**適用されます**Access 2013、Office 2013。

開いている **Connection** を閉じます。

## <a name="syntax"></a>構文

*式*です。閉じる

*式***接続**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。

代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。

