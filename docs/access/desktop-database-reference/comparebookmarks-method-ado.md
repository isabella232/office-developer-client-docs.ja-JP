---
title: comparebookmarks メソッド (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296095"
---
# <a name="comparebookmarks-method-ado"></a>comparebookmarks メソッド (ADO)

**適用先:** Access 2013、Office 2013

2 つのブックマークを比較して、相対的な位置を示す値を返します。

## <a name="syntax"></a>構文

*結果* = の*recordset*。comparebookmarks (*Bookmark1*、 *Bookmark2*)

## <a name="return-value"></a>戻り値

ブックマークで表される 2 つのレコードの相対的な行位置を示す [CompareEnum](compareenum.md) 値を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Bookmark1* |最初の行のブックマークです。|
|*Bookmark2* |2 番目の行のブックマークです。|

## <a name="remarks"></a>注釈

ブックマークは、同じ [Recordset](recordset-object-ado.md) オブジェクト、または **Recordset** オブジェクトとその [複製](clone-method-ado.md)に適用する必要があります。異なる **Recordset** オブジェクトのブックマークを比較した場合、同じソースまたはコマンドから作成されたブックマークであっても、信頼できる結果は得られません。また、基になるプロバイダーがブックマークの比較をサポートしていない **Recordset** オブジェクトの場合も、ブックマークを比較できません。

ブックマークは、 **Recordset** オブジェクトの行を一意に識別します。カレント行のブックマークを取得するには、カレント行の [Bookmark](bookmark-property-ado.md) プロパティを使用します。

ブックマークのデータ型はプロバイダー固有であり、ADO ではバリアント (Variant) 型として公開されます。 たとえば、SQL Server のブックマークは型 DBTYPE\_R8 (Double) です。 ADO では、このデータ型は、サブタイプが倍精度浮動小数点型のバリアント型として表されます。

ブックマークを比較するとき、ADO はどのような種類の強制も試みません。値は、比較が行われるプロバイダーにそのまま渡されます。 **CompareBookmarks** メソッドに渡されるブックマークが異なる型の変数に格納されている場合は、"引数が間違った型、許容範囲外、または競合しています。" という型不一致エラーが発生します。

無効なブックマークや、形式が正しくないブックマークは、エラーの原因になります。

