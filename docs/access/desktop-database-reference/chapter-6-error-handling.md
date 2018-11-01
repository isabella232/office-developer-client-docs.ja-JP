---
title: '第 6 章: エラー処理'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec3a8972f8ca46754971eee7e8aa4a70c367a349
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868330"
---
# <a name="chapter-6-error-handling"></a>第 6 章: エラー処理


**適用されます**Access 2013、Office 2013。

ADO では、発生するエラーをさまざまな方法でアプリケーションに通知します。この章では、ADO の使用時に発生する可能性のあるエラーの種類、およびアプリケーションが通知を受ける方法について説明します。最後に、それらのエラーを処理する方法に関する提案を示します。

## <a name="how-does-ado-report-errors"></a>ADO によるエラー報告の方法

ADO では、次のようなさまざまな方法でエラーが通知されます。

  - ADO エラーが発生すると、実行時エラーが生成されます。ADO エラーの処理は、Visual Basic で **On Error** ステートメントを使用するなど、他の実行時エラーと同様の方法で行います。

  - プログラムが OLE DB からエラーを受け取る場合があります。OLE DB エラーの発生時にも、実行時エラーが生成されます。

  - 発生したエラーがデータ プロバイダーに固有のものである場合、データ ソースへのアクセスに使用された **Connection** オブジェクトの **Errors** コレクションに、1 つ以上の **Error** が追加されます。

  - イベントを発生させた処理がエラーも発生させた場合、エラー情報が **Error** オブジェクトに追加され、パラメーターとしてイベントに渡されます。イベントの詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。

  - **Recordset** に関係するバッチ更新やその他の一括操作の処理時に発生した問題は、 **Recordset** の **Status** プロパティで示される場合があります。たとえば、スキーマの制約違反または権限不足は、 **RecordStatusEnum** 値で表される場合があります。

  - 現在のレコードに含まれる特定の **Field** に関する問題の発生も、 **Record** または **Recordset** の **Fields** コレクションに含まれる各 **Field** の **Status** プロパティによって示されます。たとえば、更新を完了できなかった場合や、データ型に互換性がない場合は、 **FieldStatusEnum** 値で表される場合があります。

以降のセクションでは、これらの各通知方法について詳細に説明します。

- [ADO エラー](ado-errors.md)

- [ADO のエラー リファレンス](ado-error-reference.md)

- [プロバイダー エラー](provider-errors.md)

- [フィールド関連のエラー情報](field-related-error-information.md)

- [レコードセット関連のエラー情報](recordset-related-error-information.md)

- [エラーを予測する](anticipating-errors.md)

- [他の言語でのエラーの処理 (ADO)](handling-errors-in-other-languages.md)