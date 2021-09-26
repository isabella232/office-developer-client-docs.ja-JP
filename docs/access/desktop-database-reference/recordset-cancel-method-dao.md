---
title: Recordset.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cd65395562777782b3f37a7ca3815e6113c661e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611869"
---
# <a name="recordsetcancel-method-dao"></a>Recordset.Cancel メソッド (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .キャンセル

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

Cancel メソッド **を使用** して、非同期の **Execute** メソッドまたは **OpenConnection** メソッド呼び出しの実行を終了します (つまり、メソッドは dbRunAsync オプションを使用して呼び出されました)。 **Cancel** は、終了しようとしているメソッドで dbRunAsync が使用されていない場合、実行時エラーを返します。

