---
title: Direction プロパティ (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9e34522a69b2e79f8ef44b912e2c0648c5b813d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881294"
---
# <a name="direction-property-ado"></a>Direction プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。

## <a name="remarks"></a>解説

**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。

プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。

