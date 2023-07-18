### 创建目录
```
/**
 * 创建目录（不存在创建，存在就不创建了）
 * @param dirPath 要创建的目录路径
 */
export async function mkdiruse(dirPath: PathLike) {
  if (!existsSync(dirPath)) {
    await mkdir(dirPath, { recursive: true });
  }
}
```

