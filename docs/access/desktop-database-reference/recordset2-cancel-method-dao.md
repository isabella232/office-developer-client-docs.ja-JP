---
title: Recordset2.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a7fbf84e610f57081bea30a0b6a609a11d865f13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611750"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel メソッド (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .キャンセル

*式* Recordset2 オブジェクトを **返す** 式。

## <a name="remarks"></a>注釈

Cancel メソッド **を使用** して、非同期の **Execute** メソッドまたは **OpenConnection** メソッド呼び出しの実行を終了します (つまり、メソッドは dbRunAsync オプションを使用して呼び出されました)。 **Cancel** は、終了しようとしているメソッドで dbRunAsync が使用されていない場合、実行時エラーを返します。

