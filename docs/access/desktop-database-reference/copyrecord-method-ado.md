---
title: CopyRecord メソッド (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 924df406830cf5bc1547df2bee11195b7f9e3602
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589849"
---
# <a name="copyrecord-method-ado"></a>CopyRecord メソッド (ADO)

**適用先**: Access 2013、Office 2013

**Record** で表されるエンティティを別の場所にコピーします。

## <a name="syntax"></a>構文

*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 (**String**) の値を指定します。*Source* を省略した場合、または空の文字列を指定した場合、現在の [Record](record-object-ado.md) で表されているファイルまたはディレクトリがコピーされます。|
|*宛先* |省略可能です。*Source* のコピー先の場所を指定する URL を含む文字列型 (**String**) の値を指定します。|
|*UserName* |省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。|
|*Password* |省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。|
|*Options* |省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。|
|*Async* |省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。|

## <a name="return-value"></a>戻り値

文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。

## <a name="remarks"></a>注釈

*Source* と *Destination* の値は異なっている必要があります。値が等しい場合、実行時エラーが発生します。サーバー名、パス名、リソース名のうち、少なくとも 1 つが異なっている必要があります。

*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。

*Destination* に既存のエンティティ (ファイル、ディレクトリなど) を指定する場合、**adCopyOverWrite** を指定していなければ、このメソッドは失敗します。

> [!IMPORTANT]
> Use the **adCopyOverWrite** option judiciously. たとえば、ディレクトリにファイルをコピーするときにこのオプションを指定すると、ディレクトリが削除され、ファイルに置き換えることができます。


> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


