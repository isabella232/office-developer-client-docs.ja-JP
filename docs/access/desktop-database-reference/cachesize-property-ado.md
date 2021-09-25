---
title: CacheSize プロパティ (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 70670156970f8f9a4bb52850623e145a0ee062cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558703"
---
# <a name="cachesize-property-ado"></a>CacheSize プロパティ (ADO)


**適用先:** Access 2013、Office 2013

ローカル メモリにキャッシュされる [Recordset](recordset-object-ado.md) オブジェクトのレコード数を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

0 より大きい長整数型 ( **Long** ) の値を設定または取得します。既定値は 1 です。

## <a name="remarks"></a>注釈

**CacheSize** プロパティを使用すると、プロバイダーからローカル メモリに一度に取り込むレコード数を制御できます。たとえば、 **CacheSize** が 10 の場合、 **Recordset** オブジェクトが初めて開かれた後に、最初の 10 のレコードがプロバイダーによってローカル メモリに取り込まれます。 **Recordset** オブジェクト内を移動すると、プロバイダーはローカル メモリのバッファーからデータを返します。キャッシュ内の最後のレコードより後ろのレコードに移動すると、プロバイダーはすぐに次の 10 のレコードをデータ ソースからキャッシュに取り込みます。

> [!NOTE]
> [!メモ] **CacheSize** は、プロバイダー固有のプロパティ **Maximum Open Rows** ( **Recordset** オブジェクトの **Properties** コレクション内) に基づいています。 **CacheSize** を **Maximum Open Rows** より大きい値に設定することはできません。プロバイダーが開くことのできる行の数を変更するには、 **Maximum Open Rows** を設定します。

**CacheSize** の値は、 **Recordset** オブジェクトの存続期間中に調整できますが、この値を変更しても、それ以降にデータ ソースから取得されてキャッシュに格納されるレコードの数にしか反映されません。このプロパティの値を変更しただけでは、現在のキャッシュ内の内容は変わりません。

取り込まれるレコード数が **CacheSize** で指定された数よりも少ない場合は、残りのレコードが返され、エラーは発生しません。

**CacheSize** を 0 に設定することは許可されておらず、エラーが返されます。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。すべてのキャッシュ データを強制的に更新するには、[Resync](resync-method-ado.md) メソッドを使用します。

**CacheSize** を 1 より大きい値に設定した場合は、レコードの取得後に削除が発生していると、移動メソッド ([Move](move-method-ado.md)、[MoveFirst、MoveLast、MoveNext、および MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) で削除済みのレコードに移動する可能性があります。いったん最初の取得を行うと、削除された行のデータ値にアクセスしようとしない限り、以降の削除がデータ キャッシュに反映されることはありません。一方、**CacheSize** を 1 に設定した場合は、削除された行は取得できないため、この問題を排除できます。

