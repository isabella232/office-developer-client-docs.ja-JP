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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308597"
---
# <a name="source-property-ado-error"></a>Source プロパティ (ADO Error)


**適用先:** Access 2013、Office 2013

エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。

## <a name="return-value"></a>戻り値

オブジェクトまたはアプリケーションの名前を示す文字列型 (**String**) の値を返します。

## <a name="remarks"></a>注釈

エラーが発生した元のオブジェクトまたはアプリケーションの名前を確認するには、 [error](error-object-ado.md)オブジェクトの**Source**プロパティを使用します。 これは、オブジェクトのクラス名またはプログラム ID である可能性があります。 ADO のエラーについては、プロパティの値は **ADODB. *** (objectname) になります。 *objectname*は、エラーを発生させたオブジェクトの名前です。 ADOX および ADO MD の場合、値はそれぞれ **adox. * * * objectname*および **adomd.nethttp * * objectname*となります。

**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。

**Error** オブジェクトの **Source** プロパティは読み取り専用です。

