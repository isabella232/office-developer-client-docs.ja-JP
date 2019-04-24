---
title: StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1195a45c3846cf79a45c16cda8e23bc95ef8156d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307568"
---
# <a name="recordsetstillexecuting-property-dao"></a>StillExecuting プロパティ (DAO)

**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。StillExecuting

*式***Recordset**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**StillExecuting** プロパティを使用して、直前に呼び出した非同期の **Execute** メソッドまたは **OpenConnection** メソッド (つまり、 **dbRunAsync** オプションを指定して実行したメソッド) が完了しているかどうかを調べます。 **StillExecuting** プロパティが **True** の間は、返されたオブジェクトにアクセスできません。

**StillExecuting** プロパティで **False** が取得された後で、関連付けられた **Connection** オブジェクトを返す **OpenConnection** メソッドを呼び出すと、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。

処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。

