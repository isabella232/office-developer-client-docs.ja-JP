---
title: Recordset2.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3b943bed5abdd057b21e8a1380a68231d20e00
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478052"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

## <a name="syntax"></a>構文

*式*です。キャンセル

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>備考

**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。 終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。

