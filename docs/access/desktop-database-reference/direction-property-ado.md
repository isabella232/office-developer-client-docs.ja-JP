---
title: Direction プロパティ (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293869"
---
# <a name="direction-property-ado"></a>Direction プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。

プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。

