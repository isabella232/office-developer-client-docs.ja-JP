---
title: Handler プロパティ (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292070"
---
# <a name="handler-property-rds"></a>Handler プロパティ (RDS)

**適用先:** Access 2013、Office 2013

[rdsserver.datafactory](datafactory-object-rdsserver.md)の機能を拡張するサーバー側のカスタマイズプログラム (ハンドラー) の名前と、*ハンドラー*で使用されるパラメーターを示します。

## <a name="syntax"></a>構文

*DataControl*。Handler = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |ハンドラーの名前とすべてのパラメーター (たとえば、"handlername, parm1,, parm2,..., parm *N*") を含む**文字列型 (String** ) の値を指定します。|

## <a name="remarks"></a>注釈

このプロパティは、カスタマイズをサポートしますが、この機能を使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。

ハンドラーの名前とパラメーターは、コンマ (",") で区切ります。*String* 内にセミコロン (";") が含まれていると、予期できない結果が発生する場合があります。また、**IDataFactoryHandler** インターフェイスをサポートしているハンドラーであれば、独自に作成することもできます。

既定のハンドラー名は **MSDFMAP.Handler** であり、この既定パラメーターは **MSDFMAP.INI** という名のカスタマイズ ファイルです。このプロパティは、サーバー管理者が作成した別のカスタマイズ ファイルを呼び出すときに使います。

**handler**プロパティを設定する代わりに、 [ConnectionString](connectionstring-property-ado.md)プロパティでハンドラーとパラメーターを指定することもできます。これは、"**Handler = * * * handlername, parm1,, parm2,...;*" です。

