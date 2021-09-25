---
title: QueryDef.StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: caa81317ae55e00430594b06c0f73c1c21cc5fb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568615"
---
# <a name="querydefstillexecuting-property-dao"></a>QueryDef.StillExecuting プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .StillExecuting

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

最後に呼び出した非同期の [**Execute**](querydef-execute-method-dao.md) メソッドまたは [**OpenConnection**](dbengine-openconnection-method-dao.md) メソッド (つまり、 **dbRunAsync** オプションで実行されるメソッド) が完了したかどうかを確認するには、 **StillExecuting** プロパティを使用します。 **StillExecuting** プロパティが **True** のときは、返されるオブジェクトにアクセスできません。

**StillExecuting プロパティ** が **False** を返したら、関連付けられた **[Connection](connection-object-dao.md)** オブジェクトを返す **OpenConnection** 呼び出しに続き、オブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。

処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。

