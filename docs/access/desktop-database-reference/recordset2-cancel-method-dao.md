---
title: Recordset2.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929232"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel メソッド (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。キャンセル

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>備考

**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。 終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。

