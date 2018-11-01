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
ms.openlocfilehash: 62290944381687955b19e34f728e9ffff851bcd2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872824"
---
# <a name="querydefstillexecuting-property-dao"></a>QueryDef.StillExecuting プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。StillExecuting

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

最後に呼び出した非同期の [**Execute**](querydef-execute-method-dao.md) メソッドまたは [**OpenConnection**](dbengine-openconnection-method-dao.md) メソッド (つまり、 **dbRunAsync** オプションで実行されるメソッド) が完了したかどうかを確認するには、 **StillExecuting** プロパティを使用します。 **StillExecuting** プロパティが **True** のときは、返されるオブジェクトにアクセスできません。

関連する ****Connection**** オブジェクトを取得する **OpenConnection** メソッドの呼び出しに続いて、 [StillExecuting](connection-object-dao.md) プロパティで **False** が取得されると、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。

処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。

