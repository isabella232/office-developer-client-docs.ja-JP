---
title: copyrecord メソッド (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295528"
---
# <a name="copyrecord-method-ado"></a>copyrecord メソッド (ADO)

**適用先:** Access 2013、Office 2013

**Record** で表されるエンティティを別の場所にコピーします。

## <a name="syntax"></a>構文

*レコード*。copyrecord (*Source*、 *Destination*、 *UserName*、 *Password*、 *Options*、 *Async*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 (**String**) の値を指定します。*Source* を省略した場合、または空の文字列を指定した場合、現在の [Record](record-object-ado.md) で表されているファイルまたはディレクトリがコピーされます。|
|*Destination* |省略可能です。 *Source* のコピー先の場所を指定する URL を含む文字列型 (**String**) の値を指定します。|
|*UserName* |省略可能です。 *Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。|
|*Password* |省略可能です。 *UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。|
|*Options* |省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。|
|*Async* |省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。|

## <a name="return-value"></a>戻り値

文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。

## <a name="remarks"></a>注釈

*Source* と *Destination* の値は異なっている必要があります。値が等しい場合、実行時エラーが発生します。サーバー名、パス名、リソース名のうち、少なくとも 1 つが異なっている必要があります。

*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。

*Destination* に既存のエンティティ (ファイル、ディレクトリなど) を指定する場合、**adCopyOverWrite** を指定していなければ、このメソッドは失敗します。

> [!IMPORTANT]
> Use the **adCopyOverWrite** option judiciously. たとえば、ファイルをディレクトリにコピーするときにこのオプションを指定すると、ディレクトリが*削除*され、ファイルに置き換えられます。


> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。


