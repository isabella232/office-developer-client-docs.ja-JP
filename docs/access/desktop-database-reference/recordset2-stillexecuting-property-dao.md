---
title: Recordset2.StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4816415d0f835a9f8a5b40e79ee9ed57f1b4741a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552606"
---
# <a name="recordset2stillexecuting-property-dao"></a>Recordset2.StillExecuting プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .StillExecuting

*式* Recordset2 オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

**StillExecuting** プロパティを使用して、直前に呼び出した非同期の **Execute** メソッドまたは **OpenConnection** メソッド (つまり、 **dbRunAsync** オプションを指定して実行したメソッド) が完了しているかどうかを調べます。 **StillExecuting** プロパティが **True** の間は、返されたオブジェクトにアクセスできません。

**StillExecuting** プロパティで **False** が取得された後で、関連付けられた **Connection** オブジェクトを返す **OpenConnection** メソッドを呼び出すと、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。

処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。

