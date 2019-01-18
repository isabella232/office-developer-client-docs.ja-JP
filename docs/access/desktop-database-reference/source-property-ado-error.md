---
title: Source プロパティ (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722894"
---
# <a name="source-property-ado-error"></a>Source プロパティ (ADO Error)


**適用されます**Access 2013、Office 2013。

エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。

## <a name="return-value"></a>戻り値

オブジェクトまたはアプリケーションの名前を示す文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

オブジェクトまたはアプリケーション エラーの発生源の名前を決定するのに[Error](error-object-ado.md)オブジェクトの**Source**プロパティを使用します。 これは、オブジェクトのクラス名またはプログラム id です。 ADO のエラー、プロパティの値になります **ADODB.。 ObjectName*、*オブジェクト名*は、エラーを引き起こしたオブジェクトの名前です。 ADOX および ADO MD の場合は、値となります **ADOX。。 ObjectName*および **ADOMD。。 オブジェクト名は、* それぞれ。

**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。

**Error** オブジェクトの **Source** プロパティは読み取り専用です。

