---
title: Description プロパティ (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc2a7706afbf69d9949e8b04122b144c6826ec40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882939"
---
# <a name="description-property-ado"></a>Description プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Error](error-object-ado.md) オブジェクトを記述します。

## <a name="return-value"></a>戻り値

エラーの内容を表す文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

**Description** プロパティは、エラーの簡単な説明を取得するために使います。プログラムで対処できないエラー、または処理することが望ましくないエラーは、このプロパティの内容を表示してユーザーに警告します。文字列は、ADO またはプロバイダーから渡されます。

プロバイダーは、特定のエラー テキストを ADO に渡します。ADO は、受け取ったプロバイダー エラーまたは警告ごとに [Error](error-object-ado.md) オブジェクトを **Errors** コレクションに追加します。プロバイダーが渡すエラーをトレースするには、 **Errors** コレクションを列挙します。

