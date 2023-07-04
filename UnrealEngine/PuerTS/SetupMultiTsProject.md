# 多项目设置

项目结构参考自：[ProjectReference](https://www.typescriptlang.org/docs/handbook/project-references.html#overall-structure)

## Add the “solution” tsconfig.json file

在项目的根目录中，新增一个tsconfig.json，"files"留空，"references"字段指向子目录中的tsconfig.json

下面截取自：[TypeScript源码中src/tsconfig.json](https://github.com/microsoft/TypeScript/blob/main/src/tsconfig.json)

```json
{
    "files": [],
    "include": [],
    "references": [
        { "path": "./cancellationToken" },
        { "path": "./compiler" },
    ]
}
```

## tsconfig-base.json

```json
{
  "compilerOptions": {
    "target": "esnext",
    "module": "commonjs",
    "experimentalDecorators": true,
    "jsx": "react",
    "sourceMap": true,
    "typeRoots": [
      "Plugins/Puerts/Typing",
      "Plugins/ReactUMG/Typing",
      "./node_modules/@types"
    ],
    "outDir": "../Content/JavaScript",
    "rootDir": "."
  },
  "include": [
    "TsProj/**/*"
  ],
}
```

## extends

[](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html#tsconfig-bases)