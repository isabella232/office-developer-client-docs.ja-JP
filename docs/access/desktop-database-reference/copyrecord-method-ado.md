---
title: CopyRecord メソッド (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477958"
---
# <a name="copyrecord-method-ado"></a>CopyRecord メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

**Record** で表されるエンティティを別の場所にコピーします。

## <a name="syntax"></a>構文

*レコード*です。定義 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)

## <a name="parameters"></a>パラメーター

  - *Source*

  - 省略可能です。 コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 ( **String** ) の値を指定します。 *ソース*を省略すると、空の文字列を指定する場合は、ファイルまたはディレクトリが現在の[レコード](record-object-ado.md)で表されますがコピーされます。

  - *Destination*

  - 省略可能です。 *ソース*のコピー先の場所を指定する URL を含む**文字列**値。

  - *UserName*

  - 省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。

  - *Password*

  - 省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。

  - *Options*

  - 省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。

  - *Async*

  - 省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。

## <a name="return-value"></a>戻り値

文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。

## <a name="remarks"></a>備考

*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。 サーバー、パス、またはリソースの名前の少なくとも 1 つは異なる必要があります。

*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。

**AdCopyOverWrite**を指定しない限り、*移動先*が (たとえば、ファイルまたはディレクトリ)、既存のエンティティを識別する場合、このメソッドが失敗します。


> [!IMPORTANT]
> <P><STRONG>AdCopyOverWrite</STRONG>オプションを慎重に使用します。 などのディレクトリにファイルをコピーするときにこのオプションを指定するディレクトリは<EM>削除</EM>し、ファイルで置き換えます。</P>




> [!NOTE]
> <P>[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</P>


