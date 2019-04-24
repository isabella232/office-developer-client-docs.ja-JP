---
title: Recordset2 メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307414"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2 メソッド (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。キャンセル

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。 終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。

