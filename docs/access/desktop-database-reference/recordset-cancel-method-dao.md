---
title: Recordset の Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300813"
---
# <a name="recordsetcancel-method-dao"></a>Recordset の Cancel メソッド (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。キャンセル

*式***Recordset**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。 終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。

