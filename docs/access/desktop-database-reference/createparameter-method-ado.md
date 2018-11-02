---
title: CreateParameter メソッド (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 88a5d62cc94aa707c2e90467d74dc07d80a0af02
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928944"
---
# <a name="createparameter-method-ado"></a>CreateParameter メソッド (ADO)


**適用されます**Access 2013、Office 2013。


指定したプロパティを使用して、新規 [Parameter](parameter-object-ado.md) オブジェクトを作成します。

## <a name="syntax"></a>構文

**設定***パラメーター* = *コマンド*です。CreateParameter (*名前*、*種類*、*方向*、*サイズ*、*値*)

## <a name="return-value"></a>戻り値

**Parameter** オブジェクトを返します。

## <a name="parameters"></a>パラメーター

  - *Name*

  - 省略可能です。 **Parameter** オブジェクト名を含む文字列型 ( **String** ) の値を指定します。

  - *Type*

  - 省略可能です。 [Parameter](datatypeenum.md) オブジェクトのデータ型を **DataTypeEnum** 値で指定します。

  - *Direction*

  - 省略可能です。 [Parameter](parameterdirectionenum.md) オブジェクトのデータ型を **ParameterDirectionEnum** 値で指定します。

  - *Size*

  - 省略可能です。パラメーター値の最大長を文字数またはバイト数で指定する長整数型 ( **Long** ) の値を指定します。

  - *Value*

  - 省略可能です。 **Parameter** オブジェクトの値を指定するバリアント型 ( **Variant** ) の値を指定します。

## <a name="remarks"></a>解説

**CreateParameter** メソッドを使用して、名前、種類、方向、サイズ、および値を指定して新規 **Parameter** オブジェクトを作成します。引数に指定した値は、対応する **Parameter** プロパティに書き込まれます。

このメソッドを実行しても、Parameter オブジェクトは、Command オブジェクトの Parameters コレクションに自動的に追加されません。このため、追加のプロパティを設定することができます。Parameter オブジェクトを Parameters コレクションに追加するときに、プロパティ値の妥当性が確認されます。

*型*引数で可変長データ型を指定する場合は、*サイズ*の引数を渡すか、**パラメーター**コレクションに追加する前に**Parameter**オブジェクトの[Size](size-property-ado.md)プロパティを設定それ以外の場合、エラーが発生します。

*Type* 引数に数値型 (**adNumeric** または **adDecimal**) を指定する場合は、同時に [NumericScale](numericscale-property-ado.md) プロパティと [Precision](precision-property-ado.md) プロパティも設定する必要があります。

