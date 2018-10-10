---
title: DBEngine.SetOption メソッド (DAO)
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
ms.openlocfilehash: 5e3a38cb4b35b8472b2c1af601c88af4cc9db813
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479718"
---
# <a name="dbenginesetoption-method-dao"></a>DBEngine.SetOption メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

Windows レジストリに登録されている Microsoft Access データベース エンジンのキーの値を一時的に上書きします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。SetOption (***オプション***、***値***)

*式***DBEngine**オブジェクトを返すオブジェクト式を指定します。

### <a name="parameters"></a>パラメーター

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
<td><p>オプション</p></td>
<td><p>必須</p></td>
<td><p><strong>Long 型 (Long)</strong></p></td>
<td><p>「解説」で説明している定数です。</p></td>
</tr>
<tr class="even">
<td><p>値</p></td>
<td><p>必須</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>オプションを設定する値です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

HKEY のパスに対応するレジストリ キーには、各定数\_ローカル\_マシン\\ソフトウェア\\Microsoft\\Office\\12.0\\アクセス接続エンジン\\エンジン\\(つまり、エース**dbSharedAsyncDelay**は HKEY のキーに対応する\_ローカル\_マシン\\ソフトウェア\\Microsoft\\Office\\12.0\\アクセス接続エンジン\\エンジン\\エース\\SharedAsyncDelay というように)。

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
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>SharedAsyncDelay キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>ExclusiveAsyncDelay キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>LockRetry キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>UserCommitSync キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>ImplicitCommitSync キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>MaxBufferSize キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>MaxLocksPerFile キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>LockDelay キー</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>RecycleLVs キー</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>FlushTransactionTimeout キー</p></td>
</tr>
</tbody>
</table>


**SetOption** メソッドを使用して、実行時にレジストリ値を上書きします。 **SetOption** メソッドで設定された新しい値は、 **SetOption** に対する別の呼び出しによって値が再度変更されるか、 **DBEngine** オブジェクトが閉じられるまで有効です。

