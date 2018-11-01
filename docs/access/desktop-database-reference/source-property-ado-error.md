---
title: Source プロパティ (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd8a2df4462d9f877d1b4451744fc51215227153
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875106"
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

