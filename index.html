import React, { useState } from "react";

const balanceItems = [
  { id: "concrete_abstract", category: "認知", left: "具体", right: "抽象" },
  { id: "optimism_pessimism", category: "認知", left: "楽観", right: "悲観" },
  { id: "emotion_logic", category: "欲求", left: "感情", right: "理屈" },
  { id: "stimulus_safety", category: "欲求", left: "刺激", right: "安心" },
  { id: "dominance", category: "対人関係", left: "支配", right: "被支配" },
  { id: "dependence", category: "対人関係", left: "依存", right: "自立" },
  { id: "goal_avoid", category: "動機", left: "目的志向", right: "問題回避" },
  { id: "real_ideal", category: "動機", left: "現実", right: "理想" },
  { id: "freedom", category: "適正環境", left: "自由", right: "不自由" },
];

const matrixGroups = [
  { id: "desire_matrix", category: "欲求", title: "所属意識 × 承認欲求", xLabel: "所属意識", yLabel: "承認欲求" },
  { id: "interpersonal_matrix", category: "対人関係", title: "積極性 × 孤独耐性", xLabel: "積極性", yLabel: "孤独耐性" },
];

const categoryColors = {
  認知: "#5B6B73",
  欲求: "#8B5E4A",
  対人関係: "#3D4F5C",
  動機: "#6B5B4A",
  適正環境: "#4A6B5E",
};

function BalanceSlider({ item, value, onChange }) {
  const color = categoryColors[item.category];
  return (
    <div style={{ marginBottom: 22 }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "baseline", fontSize: 14, marginBottom: 6 }}>
        <span style={{ minWidth: 64, color, fontWeight: value <= 50 ? 700 : 400, opacity: value <= 50 ? 1 : 0.5 }}>
          {item.left}
        </span>
        <span style={{ fontSize: 12, color: "#948C80" }}>
          {100 - value} : {value}
        </span>
        <span style={{ minWidth: 64, textAlign: "right", color, fontWeight: value > 50 ? 700 : 400, opacity: value > 50 ? 1 : 0.5 }}>
          {item.right}
        </span>
      </div>
      <input
        type="range"
        min="0"
        max="100"
        value={value}
        onChange={(e) => onChange(item.id, Number(e.target.value))}
        style={{ width: "100%", accentColor: color }}
      />
    </div>
  );
}

function MatrixPad({ group, x, y, onChange }) {
  const color = categoryColors[group.category];
  const size = 220;
  const px = (x / 100) * size;
  const py = size - (y / 100) * size;

  const handlePad = (e) => {
    const rect = e.currentTarget.getBoundingClientRect();
    const nx = Math.min(100, Math.max(0, ((e.clientX - rect.left) / rect.width) * 100));
    const ny = Math.min(100, Math.max(0, 100 - ((e.clientY - rect.top) / rect.height) * 100));
    onChange(group.id, Math.round(nx), Math.round(ny));
  };

  return (
    <div style={{ fontFamily: "sans-serif" }}>
      <div style={{ fontSize: 14, marginBottom: 14, fontWeight: 600, color }}>{group.title}</div>
      <div style={{ display: "flex", flexDirection: "column", alignItems: "center" }}>
        <div style={{ fontSize: 11, color: "#948C80", marginBottom: 6 }}>{group.yLabel} 強</div>
        <div
          onMouseDown={(e) => {
            handlePad(e);
            const move = (ev) => handlePad(ev);
            const up = () => {
              window.removeEventListener("mousemove", move);
              window.removeEventListener("mouseup", up);
            };
            window.addEventListener("mousemove", move);
            window.addEventListener("mouseup", up);
          }}
          style={{
            position: "relative",
            width: size,
            height: size,
            border: `1px solid ${color}55`,
            background: "#FFFDF9",
            cursor: "crosshair",
            borderRadius: 4,
          }}
        >
          <div style={{ position: "absolute", left: 0, right: 0, top: "50%", height: 1, background: "#E4DED2" }} />
          <div style={{ position: "absolute", top: 0, bottom: 0, left: "50%", width: 1, background: "#E4DED2" }} />
          <div
            style={{
              position: "absolute",
              left: px,
              top: py,
              width: 14,
              height: 14,
              borderRadius: "50%",
              transform: "translate(-50%, -50%)",
              background: color,
              boxShadow: `0 0 0 4px ${color}22`,
            }}
          />
        </div>
        <div style={{ fontSize: 11, color: "#948C80", marginTop: 6 }}>{group.yLabel} 弱</div>
      </div>
      <div style={{ display: "flex", justifyContent: "space-between", width: size, fontSize: 11, color: "#948C80", marginTop: 4 }}>
        <span>{group.xLabel} 弱</span>
        <span>{group.xLabel} 強</span>
      </div>
      <div style={{ fontSize: 12, marginTop: 10, fontWeight: 600, color }}>
        {group.xLabel} {x} ／ {group.yLabel} {y}
      </div>
    </div>
  );
}

export default function InterpersonalProfile() {
  const [balances, setBalances] = useState(
    Object.fromEntries(balanceItems.map((i) => [i.id, 50]))
  );
  const [matrices, setMatrices] = useState(
    Object.fromEntries(matrixGroups.map((g) => [g.id, { x: 50, y: 50 }]))
  );

  const updateBalance = (id, value) => setBalances((prev) => ({ ...prev, [id]: value }));
  const updateMatrix = (id, x, y) => setMatrices((prev) => ({ ...prev, [id]: { x, y } }));

  const categories = ["認知", "欲求", "対人関係", "動機", "適正環境"];

  return (
    <div style={{ fontFamily: "serif", background: "#FAF8F4", color: "#2A2826", minHeight: "100vh", padding: "48px 24px 80px" }}>
      <div style={{ maxWidth: 780, margin: "0 auto 56px" }}>
        <h1 style={{ fontSize: 28, fontWeight: 600, margin: "0 0 8px" }}>対人分析プロフィール</h1>
        <p style={{ fontFamily: "sans-serif", fontSize: 13, color: "#6B655E", margin: 0, lineHeight: 1.7 }}>
          各項目のスライダーとパッドを操作して、自分自身、または分析したい人物のプロフィールを組み立てます。
        </p>
      </div>

      {categories.map((cat) => {
        const items = balanceItems.filter((i) => i.category === cat);
        const groups = matrixGroups.filter((g) => g.category === cat);
        if (items.length === 0 && groups.length === 0) return null;
        return (
          <div key={cat} style={{ maxWidth: 780, margin: "0 auto 48px", borderTop: "1px solid #E4DED2", paddingTop: 24 }}>
            <div style={{ fontFamily: "sans-serif", fontSize: 12, letterSpacing: "0.15em", marginBottom: 20, display: "flex", alignItems: "center", gap: 10, color: categoryColors[cat] }}>
              <span style={{ width: 8, height: 8, borderRadius: "50%", background: categoryColors[cat], display: "inline-block" }} />
              {cat}
            </div>

            {items.map((item) => (
              <BalanceSlider key={item.id} item={item} value={balances[item.id]} onChange={updateBalance} />
            ))}

            {groups.length > 0 && (
              <div style={{ display: "flex", gap: 48, flexWrap: "wrap" }}>
                {groups.map((g) => (
                  <MatrixPad key={g.id} group={g} x={matrices[g.id].x} y={matrices[g.id].y} onChange={updateMatrix} />
                ))}
              </div>
            )}
          </div>
        );
      })}
    </div>
  );
}
