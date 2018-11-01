---
title: Recordset2.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62bd5f60ed48e863a5190a19e546d292156f8dac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888336"
---
# <a name="recordset2close-method-dao"></a>Recordset2.Close メソッド (DAO)


**適用されます**Access 2013、Office 2013。

開いている **Recordset** を閉じます。

## <a name="syntax"></a>構文

*式*です。閉じる

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。

開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。

代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。

