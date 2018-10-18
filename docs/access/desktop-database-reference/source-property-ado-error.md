---
title: Source プロパティ (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adeadcf4c467aabad7b486bd43c12e26d67ce302
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603867"
---
# <a name="source-property-ado-error"></a>Source プロパティ (ADO Error)


**適用されます**Access 2013 |。Office 2013

エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

オブジェクトまたはアプリケーションの名前を示す文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

オブジェクトまたはアプリケーション エラーの発生源の名前を決定するのに[Error](error-object-ado.md)オブジェクトの**Source**プロパティを使用します。 これは、オブジェクトのクラス名またはプログラム id です。 ADO のエラー、プロパティの値になります **ADODB.。 ObjectName*、*オブジェクト名*は、エラーを引き起こしたオブジェクトの名前です。 ADOX および ADO MD の場合は、値となります **ADOX。。 ObjectName*および **ADOMD。。 オブジェクト名は、* それぞれ。

**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。

**Error** オブジェクトの **Source** プロパティは読み取り専用です。

