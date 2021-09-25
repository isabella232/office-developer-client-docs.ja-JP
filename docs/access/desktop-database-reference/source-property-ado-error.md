---
title: Source プロパティ (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ebaf5f3a9e0c8ae005c21b0872177e0699c0f9aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568419"
---
# <a name="source-property-ado-error"></a>Source プロパティ (ADO Error)


**適用先:** Access 2013、Office 2013

エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。

## <a name="return-value"></a>戻り値

オブジェクトまたはアプリケーションの名前を示す文字列型 (**String**) の値を返します。

## <a name="remarks"></a>注釈

Error オブジェクト **の Source** プロパティ [を使用](error-object-ado.md) して、最初にエラーを生成したオブジェクトまたはアプリケーションの名前を特定します。 これは、オブジェクトのクラス名またはプログラム ID です。 ADO のエラーの場合、プロパティの値は **ADODB になります。** *ObjectName*、 *ObjectName* は、エラーをトリガーしたオブジェクトの名前です。 ADOX と ADO MD の場合、値は **ADOX になります。** *ObjectName* と **ADOMD。** *それぞれ ObjectName。*

**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。

**Error** オブジェクトの **Source** プロパティは読み取り専用です。

