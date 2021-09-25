---
title: Size プロパティ (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f4814d06cbf93f8055ba7830f3cc8c2ad7090cbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593552"
---
# <a name="size-property-ado"></a>Size プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Parameter](parameter-object-ado.md) オブジェクトの最大サイズをバイト数または文字数で示します。

## <a name="settings-and-return-values"></a>設定および戻り値

**Parameter** オブジェクトの最大サイズをバイト数または文字数で示す長整数型 (**Long**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Parameter** オブジェクトの [Value](value-property-ado.md) プロパティで設定または取得できる値の最大サイズを調べるには、**Size** プロパティを使用します。

**Parameter** オブジェクトとして可変長データ型 (たとえば、**adVarChar** などのすべての文字列型 (**String**)) を指定した場合、[Parameters](parameters-collection-ado.md) コレクションにそのオブジェクトを追加する前に、オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。

**Parameter** オブジェクトが **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションに既に追加されている場合に、そのデータ型を可変長データ型に変更した場合は、 **Command** オブジェクトを実行する前に **Parameter** オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。

[Refresh](refresh-method-ado.md) メソッドを使用してプロバイダーからパラメーター情報を取得したときに、可変長データ型の **Parameter** オブジェクトが返された場合、可能な最大サイズに基づいてパラメーターにメモリが割り当てられますが、これが原因で実行時にエラーが発生することがあります。エラーを回避するには、コマンドを実行する前に、明示的にこれらのパラメーターの **Size** プロパティを設定します。

**Size** プロパティは、値の取得および設定が可能です。

