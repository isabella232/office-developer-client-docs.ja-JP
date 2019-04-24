---
title: DBEngine メソッド (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294198"
---
# <a name="dbenginesetoption-method-dao"></a>DBEngine メソッド (DAO)

**適用先:** Access 2013、Office 2013

Windows レジストリに登録されている Microsoft Access データベース エンジンのキーの値を一時的に上書きします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。SetOption (***オプション***、***値***)

*式***DBEngine**オブジェクトを返すオブジェクト式を指定します。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Long 型 (Long)</strong></p></td>
<td><p>「解説」で説明している定数です。</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>オプションに設定する値を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

各\_定数は、パス HKEY ローカル\_コンピューター\\ソフトウェア\\の Microsoft\\Office\\12.0\\access Connectivity Engine Engine\\\\ACE (つまりは、**dbsharedasyncdelay**は\_キーの HKEY ローカル\_コンピューター\\ソフトウェア\\Microsoft\\Office\\12.0\\access Connectivity Engine\\エンジン\\ACE に対応します。\\sharedasyncdelay など)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>PageTimeout キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsharedasyncdelay</strong></p></td>
<td><p>SharedAsyncDelay キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>ExclusiveAsyncDelay キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dblockretry</strong></p></td>
<td><p>LockRetry キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbusercommitsync</strong></p></td>
<td><p>UserCommitSync キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>ImplicitCommitSync キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbmaxbuffersize</strong></p></td>
<td><p>MaxBufferSize キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>MaxLocksPerFile キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblockdelay</strong></p></td>
<td><p>LockDelay キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>RecycleLVs キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbflushtransactiontimeout</strong></p></td>
<td><p>FlushTransactionTimeout キー</p></td>
</tr>
</tbody>
</table>


**SetOption** メソッドを使用して、実行時にレジストリ値を上書きします。 **SetOption** メソッドで設定された新しい値は、 **SetOption** に対する別の呼び出しによって値が再度変更されるか、 **DBEngine** オブジェクトが閉じられるまで有効です。

