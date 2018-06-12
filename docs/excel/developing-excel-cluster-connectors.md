---
title: Excel �N���X�^�[ �R�l�N�^�̊J��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798763"
---
# <a name="developing-excel-cluster-connectors"></a>Excel �N���X�^�[ �R�l�N�^�̊J��

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Excel �N���X�^�[ �R�l�N�^�́AXLL ��̃N���X�^�[ �Z�[�t�̃��[�U�[��[](cluster-safe-functions.md)�֐��̏ڍׂɂ��ẮA�u[�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)�v��Q�Ƃ��Ă��������B���̃I�t���[�h�ɂ��A����ɑ����̃R���s���[�e�B���O ���\�[�X��g�p�ł���悤�ɂ��āA�p�t�H�[�}���X����サ�܂��B�ʏ�A�N���X�^�[ �R�l�N�^�́A�����\�v�Z�N���X�^�[�̃x���_�[�ɂ���ĊJ������܂��B
  
## <a name="cluster-connectors"></a>�N���X�^�[ �R�l�N�^

クラスター コネクタは定義済みのエントリ ポイントを提供する DLL です。Excel では、このエントリ ポイントを使用して、クラスター セーフなユーザー定義関数の呼び出しを調整します。これは Excel と高性能計算クラスター間のインターフェイスとして、セッションを管理したり、関数呼び出しを実行 (完全修飾の関数名と呼び出しの実引数を渡すことによる) したり、コールバック メカニズムを使用して Excel に呼び出しの結果を返すために使用します。
  
�N���X�^�[ �R�l�N�^��쐬����ɂ́ADLL ��쐬���āA�u[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)�v�ɋL�ڂ���Ă���G���g�� �|�C���g����J���܂��B
  
## <a name="installing-a-cluster-connector"></a>�N���X�^�[ �R�l�N�^�̃C���X�g�[��

�N���X�^�[ �R�l�N�^�� Excel �Ŏg�p�\�ɂ���ɂ́A�R�l�N�^�̃Z�b�g�A�b�v �R�[�h�ŁAExcel ���C���X�g�[������Ă���R���s���[�^�[�ɃR�l�N�^�� DLL ��C���X�g�[������K�v������܂��B����ɁA�R�l�N�^�̃Z�b�g�A�b�v �R�[�h�́A�R�l�N�^�̃G���g������̃��W�X�g�� �L�[�̉��ɒǉ�����K�v������܂��B
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
���̃N���X�^�[ �R�l�N�^�̃L�[�ɁA���̕������w�肷��m�[�h��ǉ����܂��B
  
-  `Name`? Excel ��̃N���X�^�[ �R�l�N�^�̈ꗗ�ɕ\������閼�O�B
    
-  `Filename`? DLL �̊��S�p�X�B
    

