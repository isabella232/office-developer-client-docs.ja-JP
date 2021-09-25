---
title: GetChildren メソッド (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6c2c23ed24ecde11e182e623834f986a37b9e73f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573006"
---
# <a name="getchildren-method-ado"></a>GetChildren メソッド (ADO)


**適用先:** Access 2013、Office 2013


各行がコレクション [Record](record-object-ado.md) の子を表す [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

**レコードセット***レコードを*  =  *設定します*。GetChildren

## <a name="return-value"></a>戻り値

各行が現在の **Record** オブジェクトの子を表す **Recordset** オブジェクトを返します。たとえば、ディレクトリを表す **Record** の子は、親ディレクトリに含まれるファイルとサブディレクトリです。

## <a name="remarks"></a>注釈

返される **Recordset** にどのような列があるかは、プロバイダーによって決まります。たとえば、ドキュメント ソース プロバイダーは、常にリソースの **Recordset** を返します。

