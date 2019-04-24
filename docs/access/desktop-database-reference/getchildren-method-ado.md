---
title: getchildren メソッド (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292308"
---
# <a name="getchildren-method-ado"></a>getchildren メソッド (ADO)


**適用先:** Access 2013、Office 2013


各行がコレクション [Record](record-object-ado.md) の子を表す [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

**設定***recordset* = *レコード*。GetChildren

## <a name="return-value"></a>戻り値

各行が現在の **Record** オブジェクトの子を表す **Recordset** オブジェクトを返します。たとえば、ディレクトリを表す **Record** の子は、親ディレクトリに含まれるファイルとサブディレクトリです。

## <a name="remarks"></a>注釈

返される **Recordset** にどのような列があるかは、プロバイダーによって決まります。たとえば、ドキュメント ソース プロバイダーは、常にリソースの **Recordset** を返します。

