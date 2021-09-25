---
title: QueryDef.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6c404f493072974632bfdd155fc2664258721867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558045"
---
# <a name="querydefcancel-method-dao"></a>QueryDef.Cancel メソッド (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .キャンセル

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

Cancel メソッド **を使用** して、非同期の **Execute** メソッドまたは **OpenConnection** メソッド呼び出しの実行を終了します (つまり、メソッドは dbRunAsync オプションを使用して呼び出されました)。 **Cancel** は、終了しようとしているメソッドで dbRunAsync が使用されていない場合、実行時エラーを返します。

